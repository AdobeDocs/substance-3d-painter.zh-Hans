---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/pipeline-and-integration/installation-and-preferences/automated-installation.html"
breadcrumb-title: ''
description: 了解如何针对企业部署和管道集成工作流自动化Substance 3D Painter安装。
helpx_creative_field: ""
helpx_description: Painter > Pipeline and integration > Installation and preferences > Automated installation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 自动安装
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---


# 自动安装

使用Substance 3D独立安装程序时，可以在静默模式下安装应用程序，以方便部署。

我们正在使用&#x200B;**InnoSetup**&#x200B;生成安装程序。 此处提供了可用于安装程序的整组参数[](http://www.jrsoftware.org/ishelp/index.php?topic=setupcmdline)。

## 通过命令行以静默模式安装

用于执行静默安装的标志为&#x200B;**/SILENT**。 标志&#x200B;**/NCRC**&#x200B;还可以用于跳过包的CRC（验证）以加快进程。

示例：

```
SubstancePainter_Installer.exe /NCRC /SILENT /DIR="C:InstallationFolder"
```


>[!NOTE]
>
> 安装路径必须使用单个反斜杠字符来分隔文件夹，否则安装程序将无法识别该路径。
