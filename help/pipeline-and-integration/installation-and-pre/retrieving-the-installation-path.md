---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/pipeline-and-integration/installation-and-preferences/retrieving-the-installation-path.html"
breadcrumb-title: ''
description: 了解如何检索Substance 3D Painter的安装路径以用于脚本和管道集成目的。
helpx_creative_field: ""
helpx_description: Painter > Pipeline and integration > Installation and preferences > Retrieving the installation path
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 检索安装路径
user-guide-description: ''
user-guide-title: ''
source-git-commit: 22871eab2f25d09bd82f1292d8b3e5f8c4f1c2cf
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 6%

---


# 检索安装路径

本页根据版本和平台，对检索应用程序安装路径的方法进行了重新分组。

## Windows

### Creative Cloud 桌面版

1. 打开Windows注册表编辑器(**regedit**)。
1. 导航到注册表项： **&#x200B; HKEY\_LOCAL\_MACHINE\Software\Microsoft\Windows\CurrentVersion\App Paths\**
1. 打开名为&#x200B;**Adobe Substance 3D Painter.exe**&#x200B;的子密钥
1. 密钥的值包含安装该密钥的应用程序可执行文件的路径

>[!NOTE]
>
> 此注册表项仅从版本7.2开始可用。\
>  对于旧版本，可从&#x200B;**HKEY\_CURRENT\_USER\Software\Microsoft\Windows\CurrentVersion\ Explorer\FileExts**&#x200B;中的文件关联检索安装路径。

### Substance 3D Standalone

1. 打开Windows注册表编辑器(**regedit**)。
1. 导航到注册表项： **HKEY\_LOCAL\_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall**
1. 查找与应用程序版本的AppID匹配的子项（请参阅下表）
1. 密钥的值包含应用程序安装位置的路径

| Version | AppId |
| --- | --- |
| **版本1.x** | `{410F5B6E-A29C-4F43-9DE3-44A1357D6AF5}` |
| **版本2.x** | `{f42b7a996fa1d13a1d0a2e33eea2c0800bb5d1b8}` |
| **3.x (2017.x)至7.1** | `{33C3E9E2-0675-4196-9019-28AB9C5E9BB0}` |
| **7.2或更高版本** | `{2a8bbb68-725b-477c-9194-60efc5ece348}` |

### 蒸汽

应用程序安装在Steam安装文件夹的&#x200B;**steamapps/common/**&#x200B;子文件夹中。

## Mac

在Mac上，该应用程序安装在以下软件中：

| Version | 路径 |
| --- | --- |
| **7.2或更高版本** | **/Applications/Adobe Substance 3D Painter.app** |
| **旧版** | **/Applications/Substance Painter.app** |

## Linux

在Linux上， rpm软件包安装在以下路径中：

| Version | 路径 |
| --- | --- |
| **7.2或更高版本** | **/opt/Adobe/Adobe\_Substance\_3D\_Painter** |
| **旧版** | **/opt/Allegorithmic/Substance\_Painter** |
