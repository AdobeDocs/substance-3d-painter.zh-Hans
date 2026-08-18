---
source-git-commit: 0376fe6500551442b28831d5742ecbbc9363ab19
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 1%

---
# 已知问题生成器 — Substance 3D Painter

自动为Substance 3D Painter生成已知问题标记文档，发布位置为：
`https://helpx.adobe.com/substance-3d-painter/release-notes/know-issues.html`

问题源自Jira史诗`SBSFOUR-6267`。 该脚本会获取所有问题，过滤掉目标版本中已修复的任何内容，并输出准备提交的格式化标记文件。

&#x200B;---

## 快速开始

这些步骤假定您已经完成下面的一次性设置。

1. 连接到&#x200B;**GlobalProtect VPN**
2. 将`.env`文件中的`TARGET_VERSION`设置为要为其生成文档的版本（例如`12.0.3`）
3. 从`scripts/known-issues-automation/`目录运行脚本：

   ```
   python fetch_known_issues.py
   ```

4. 查看输出摘要 — 它将报告获取的问题数和排除的问题数
5. 将生成的`known-issues.md`复制到`help/release-notes/known-issues.md`

> 如果丢失任何问题或出现意外问题，请在应用筛选之前检查`raw_issues.json`以准确查看Jira返回的内容。

&#x200B;---

## 一次性设置

### &#x200B;1. 安装依赖项

```bash
pip install requests python-dotenv
```

### &#x200B;2. 创建您的`.env`文件

```bash
cp .env.example .env
```

### &#x200B;3. 获取Jira个人访问令牌

1. 登录`https://jira.corp.adobe.com`
2. 在左侧边栏中→**个人访问令牌**&#x200B;转到您的个人资料
3. 单击&#x200B;**创建令牌**，为其指定名称并复制生成的值

> 在您的浏览器会话结束时，PAT不会过期，因此对于脚本式API访问，PAT比会话Cookie更可靠。

### &#x200B;4. 填写您的`.env`文件

```
JIRA_PAT=your-personal-access-token
TARGET_VERSION=12.0.3
OUTPUT_FILE=known-issues.md
```

`TARGET_VERSION`是您为其生成已知问题页面的Substance 3D Painter版本。 它控制排除哪些已修复的问题 — 请参阅下面的[筛选逻辑](#filtering-logic)。

&#x200B;---

## 存储库结构

```
.
├── README.md                  # This file
├── fetch_known_issues.py      # Main script
├── .env.example               # Environment variable template (safe to commit)
├── .env                       # Your local credentials — never commit this
├── raw_issues.json            # Raw Jira dump from last run — gitignored
└── known-issues.md            # Generated output from last run — gitignored
```

&#x200B;---

## Jira Reference

| 字段 | Value |
|---|---|
| Jira实例 | `https://jira.corp.adobe.com` |
| 项目密钥 | `SBSFOUR` |
| 史诗般的已知问题 | `SBSFOUR-6267` |

所有已知问题都必须与此史诗链接，才能在生成的文档中显示。 如果需要向页面添加问题或从页面中删除问题，请在Jira中更新epic，而不是手动编辑markdown。

&#x200B;---

## 脚本的工作方式

### 第1步 — 获取

该脚本使用JQL查询Jira REST API：

```
"Epic Link" = SBSFOUR-6267 ORDER BY created ASC
```

结果以每页50期的分页显示。 为每个问题检索了以下字段： `summary`、`issuetype`、`status`、`affectedVersions`、`fixVersions`、`labels`。

身份验证使用来自`JIRA_PAT`的持有者令牌。 企业Jira实例使用内部SSL证书，因此对这些请求禁用证书验证 — 这在Adobe网络上是预期的行为。

### 第2步 — 原始转储

在筛选或格式化之前，脚本将写入`raw_issues.json`。 这是Jira返回的每个问题的简化快照，无论接下来发生什么情况，始终生成该快照。 如果输出看起来有误，请先检查此文件 — 它确切显示了Jira提供的数据。

### 第3步 — 筛选

可通过同时应用的两个规则过滤问题：

1. **状态筛选器** — 只有`Backlog`和`Dev In Progress`个问题属于活动已知问题。 状态`Fixed`的问题是候选排除项，需接受下面的版本检查。

2. **版本筛选器** — 仅当其修复版本之一小于或等于`TARGET_VERSION`时，才排除`Fixed`问题。 如果修复版本高于`TARGET_VERSION`，则问题仍包括在内，因为尚未针对所记录的版本发布修复。

这处理了同时开发两个版本的情况： `12.1.0`中修复的问题仍然是`12.0.3`的已知问题。

有关完整的决策表，请参阅[筛选逻辑](#filtering-logic)。

### 第4步 — 分析类别

每个问题摘要在字符串开头都会针对类别标记进行分析：

- `[Shader] Some description`→类别： `["Shader"]`，描述： `"Some description"`
- `[Crash][Engine] Some description`→类别： `["Crash", "Engine"]`，描述： `"Some description"`
- `No brackets here`没→类别，被视为未分类

**主要类别**&#x200B;始终是第一个标签。 它决定分组和截面放置。

### 第5步 — 分组和排序

问题安排如下：

- 问题按主要类别分组
- 组按问题数排序，降序排列（最大组优先）
- 有多个问题的组显示在文档顶部
- 只有一个问题的组以及任何未分类的问题会出现在没有节标题的多问题组之后
- `[Crash]`作为其主要类别的问题始终放在最后，位于`## Stability`部分下

### 第6步 — 格式化和写入

脚本输出`known-issues.md`，其内容为：

- YAML前页（helpx元数据）
- `# Known issues`标题，其中包含命名目标版本的说明段落
- 问题格式为： `` * `[Category]` Description ``
- 多类别问题： `` * `[Category1]` `[Category2]` Description ``
- 类别组之间的空白行
- 结尾处有一个`## Stability`部分，介绍崩溃问题

&#x200B;---

## 过滤逻辑

| 状态 | 是否修复版本集？ | 修复版本与目标 | 是否包括？ |
|---|---|---|---|
| `Backlog` | — | — | 是 |
| `Dev In Progress` | — | — | 是 |
| `Fixed` | 否 | — | 否（保守地排除） |
| `Fixed` | 是 | 修复目标≤版本 | 无（已发货） |
| `Fixed` | 是 | 修复版本>目标 | 是（未来版本中会进行修复） |

&#x200B;---

## 输出格式

```markdown
---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/release-notes/know-issues.html"
...
---

# Known issues

This page lists all the active known issues present in v12.0.3 of Substance 3D Painter:

* `[Engine]` Error when using Smart Materials if Texture Set has no tile 1001
* `[Engine]` Geometry mask shows artifacts at UV borders with instanced layers

* `[Shader]` user0 channel always can not be read as sRGB with specific shader

* `[Export]` GLTF exports at the wrong size
* `[Import]` Cannot import obj file with "nan" values

## Stability

* `[Crash]` Select "Export mesh" when mesh failed to load
```

**设置注释格式：**&#x200B;类别标签使用单后置循环 — `` `[Category]` `` — 而不是双后置循环。 手动维护的旧版文档包含双回拨错误；脚本始终生成正确的格式。

&#x200B;---

## 故障排除

**401未授权**
- 确认您已连接到&#x200B;**GlobalProtect VPN**
- 您的PAT可能已过期或已撤销 — 请在`https://jira.corp.adobe.com/secure/ViewProfile.jspa`生成新的PAT并更新您的`.env`

**`JIRA_PAT is not set`错误**
- 确保您已从`.env.example`创建`.env`文件并填写您的令牌
- 确认正在从`scripts/known-issues-automation/`目录中运行脚本，以便`python-dotenv`可以找到`.env`文件

**输出中缺少问题**
- 检查`raw_issues.json` — 如果不存在该问题，则表明它未与Jira中的epic `SBSFOUR-6267`关联
- 如果问题在`raw_issues.json`中但不在输出中，则会被筛选器排除 — 请检查其状态并修复您的`TARGET_VERSION`版本

运行时&#x200B;**出现**`TARGET_VERSION`&#x200B;警告
- 脚本将运行，但如果未设置`TARGET_VERSION`，则保守地排除所有`Fixed`问题。 请始终在生成最终文档之前进行设置。
