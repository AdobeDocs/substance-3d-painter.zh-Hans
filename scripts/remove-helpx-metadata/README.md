---
source-git-commit: 6b6d52207ca1d043aaa1b2b14145b6b49d4c1942
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%
---
# 删除旧版HelpX元数据

使用Python 3.10或更高版本，从存储库根目录运行以下命令：

```shell
python remove_helpx_metadta.py 1 <path>
python remove_helpx_metadta.py 2 <path>
```

模式`1`是模拟运行：它列出匹配的文件并报告文件数
扫描的文件、具有匹配项的文件以及匹配的元数据字段，而不更改文件。
模式`2`删除这些字段并报告删除计数。 省略`<path>`以
扫描当前文件夹。 引用包含空格的路径。

脚本递归扫描`.md`个文件（不区分大小写）并删除顶级
名称以`helpx`开头的YAML前导字段，包括其多行
值。 它保留其他元数据、注释、空白行、Markdown内容
编码和行尾。 它不会删除正文中的`helpx`引用。
在使用模式`2`之前查看模拟运行；删除编辑文件而不使用
创建备份。 报告并生成文件错误和未关闭的前页
非零退出状态。 包含未关闭的前部内容的文件将保持不变。