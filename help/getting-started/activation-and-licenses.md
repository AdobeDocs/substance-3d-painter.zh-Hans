---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/getting-started/activation-and-licenses.html"
breadcrumb-title: ''
description: 了解如何激活Substance 3D Painter并管理许可证以开始使用应用程序进行纹理绘画。
helpx_creative_field: ""
helpx_description: Painter > Getting Started > Activation and licenses
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 激活和许可证
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 1%

---


# 激活和许可证

此页面包含有关如何激活和管理许可证的信息，以便您可以开始使用Painter。

## 每个应用程序类型的激活流程

激活过程取决于您购买或有权访问Painter的位置：

| 应用程序类型 | 激活过程 |
| --- | --- |
| Creative Cloud 桌面版 | 请参阅[HelpX文档](https://helpx.adobe.com/download-install/using/download-creative-cloud-apps.html)中的专用页面。 如果有任何问题，[Creative Cloud文档](https://helpx.adobe.com/creative-cloud/user-guide.html)可能会提供其他答案。 |
| 蒸汽 | 直接从Steam库中启动产品。 |
| Substance 3D独立 | 请参阅下述激活流程。 |

## 独立激活步骤

### 激活向导

在某些旧版Substance 3D Painter中会显示“激活向导”。

如果您在2022年9月30日之前从Substance 3D网站下载了永久许可证文件，则您仍然可以通过激活向导使用该文件激活符合条件的Substance 3D Painter版本。 [此处提供了有关旧版Substance许可证和帐户的更多信息。](https://substance3d.adobe.com/faq-end-of-life-accounts/)

![](../assets/activation-wizard.png){width="350px"}

激活向导有3个选项：

* <b>评估此产品</b>：旧版试用不再可用。 而是可以[在此处为每个Substance 3D应用程序开始30天试用](https://www.adobe.com/products/substance3d/free-trial-download.html?msockid=35568f9be2b964ec22d09c04e3eb65af)或使用Creative Cloud桌面版。
* <b>使用许可证文件进行激活</b>：在2022年9月30日之前，使用从Substance 3D网站上的帐户页面下载的许可证文件(<b>\*.key</b>)激活产品。
* <b>使用您的帐户激活</b>：旧版Substance帐户无法再用于激活。

>[!WARNING]
>
> 要使用“激活向导”安装许可证文件，请确保以管理员身份运行Painter并暂时禁用防病毒软件。

### 手动激活

您可以通过将license.key文件放入以下文件夹来手动激活Substance Painter：

>[!NOTE]
>
> 确保该文件名为&#x200B;**license.key**，否则应用程序将无法找到它。

<table data-preserve-html="true"><colgroup> <col/> <col/> <col/> <col/> </colgroup><tbody><tr><th>Platform</th><th>Version</th><th colspan="2">路径</th></tr><tr><td rowspan="4"><strong>Windows</strong></td><td rowspan="2"><strong>7.2</strong>或更高版本</td><td colspan="1">应用程序数据（本地）</td><td colspan="1">C:\Users\用户\[用户名]\AppData\Local\Adobe\Adobe Substance 3D Painter</td></tr><tr><td colspan="1">应用程序数据（漫游）</td><td colspan="1">C:\Users\用户\[用户名]\AppData\Roaming\Adobe\Adobe Substance 3D Painter</td></tr><tr><td rowspan="2">旧版</td><td colspan="1">应用程序数据（本地）</td><td colspan="1">C:\Users\用户\[用户名]\AppData\Local\Allegorithmic\Substance Painter</td></tr><tr><td colspan="1">应用程序数据（漫游）</td><td colspan="1">C:\Users\用户\[用户名]\AppData\Roaming\Allegorithmic\Substance Painter</td></tr><tr><td rowspan="2"><strong>Mac</strong></td><td colspan="1"><strong>7.2</strong>或更高版本</td><td colspan="2">/用户/[用户名]/资源库/Application Support/Adobe/Adobe Substance 3D Painter</td></tr><tr><td colspan="1">旧版</td><td colspan="2">/用户/[用户名]/资源库/Application Support/Allegorithmic/Substance Painter</td></tr><tr><td rowspan="2"><strong>Linux</strong></td><td colspan="1"><strong>7.2</strong>或更高版本</td><td colspan="2">/home/[用户名]/.local/share/Adobe/Adobe Substance 3D Painter</td></tr><tr><td>旧版</td><td colspan="2">/home/[用户名]/.local/share/Allegorithmic/Substance Painter</td></tr></tbody></table>

>[!NOTE]
>
> 上述路径中的某些目录可能默认处于隐藏状态。 在文件资源管理器中手动键入路径，或者显示隐藏的文件以查看它们。

### 环境变量

您可以使用[环境变量](../pipeline-and-integration/configuration/environment-variables.md)覆盖Painter为&#x200B;**license.key**&#x200B;文件检查的位置。
