---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/technical-issues/startup-issues/crash-or-freeze-during-startup.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter启动期间修复崩溃和冻结问题，以稳定启动应用程序。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > Startup Issues > Crash or freeze during startup
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 启动期间崩溃或冻结
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 0%

---


# 启动期间崩溃或冻结

本页列出了与应用程序无法正确启动相关的已知问题及其解决方案。

## 软件冲突

请查看以下页面，获取可能引发冲突的所有已知软件的列表： [软件冲突](software-conflicts.md)。

## 在错误的GPU上运行

如果应用程序没有在正确的GPU上启动，则可能会导致稳定性问题。 请参阅此页面了解更多信息： [Painter未在右GPU上启动](../gpu-issues/painter-doesn-t-start-on-the-right-gpu.md)。

## 过时的GPU驱动程序

使用旧版GPU驱动程序可能导致冻结和/或崩溃。 我们建议尽可能使用最新的GPU驱动程序。 请参阅： [GPU具有过时的驱动程序](../gpu-issues/gpu-has-outdated-drivers.md)。

## 白屏且无响应

如果在Windows上启动时应用程序冻结（导致出现白屏），可能是以下原因造成的：

* 外部应用程序正在产生冲突，请参阅[软件冲突](software-conflicts.md)以了解哪些冲突。
* 该应用程序的某些窗口已在另一个监视器上打开。 将界面恢复为默认布局后，可以正常启动应用程序：
  1. 从开始菜单中打开注册表编辑器(**regedit**)
  1. 导航到应用程序首选项（请参阅： [首选项和应用程序数据位置](https://helpx.adobe.com/substance-3d/unlisted/documentation/spdoc/application-preferences-location-147095594.html)）
  1. 展开&#x200B;**Adobe Substance 3D Painter**&#x200B;项
  1. 选择&#x200B;**主窗口2018**&#x200B;键并将其删除
  1. 重新启动应用程序

## 由于不正确的系统路径/Python路径而崩溃

应用程序会检查系统Path以加载Python模块和环境设置。 如果系统设置不正确，则可能会导致在启动过程中崩溃。

在Windows上：

1. 打开&#x200B;**开始**&#x200B;菜单
1. 搜索并选择&#x200B;**系统（控制面板）**
1. 单击&#x200B;**高级系统设置**
1. 单击&#x200B;**环境变量**
1. 在&#x200B;**系统变量**&#x200B;下找到&#x200B;**PATH**&#x200B;变量

然后，可以编辑变量以验证其内容。 例如，如果变量包含此类以下字符，则会导致崩溃

```
ï–›éŒ à €è¸€ì‡ì‡ç¿¹
```


## Windows 10更新

Windows 10的某些更新有时可能会导致不稳定。 使用Windows附带的诊断工具检测系统中任何潜在的错误。

我们建议运行&#x200B;**部署映像服务和管理** (DISM)和&#x200B;**系统文件检查器** (SFC)工具。 DISM可用于恢复SFC所需的替换文件，以便修复损坏或丢失的系统文件。

正在运行&#x200B;**DISM** ：

1. 打开“开始”菜单
1. 搜索命令提示符
1. 右键单击结果，然后选择“以管理员身份运行”
1. 键入以下命令： **DISM /Online /Cleanup-Image /RestoreHealth**
1. 按Enter

正在运行&#x200B;**SFC** ：

1. 打开“开始”菜单
1. 搜索命令提示符
1. 右键单击结果，然后选择“以管理员身份运行”
1. 键入以下命令： **sfc /scannow**
1. 按Enter

使用这两个命令后重新启动计算机以应用更新。

有关此主题的详细信息，请参阅： [使用系统文件检查器工具修复丢失或损坏的系统文件](https://support.microsoft.com/en-us/help/929833/use-the-system-file-checker-tool-to-repair-missing-or-corrupted-system)。

## 在旧版本上启动时崩溃

在Windows上，版本2018 (4.x)或更早版本可能无法启动，因为安装文件夹提供的dll文件之一对于操作系统来说太旧。 可通过手动将该文件替换为较新版本来修复此崩溃问题。

具体操作如下：

1. 导航到Substance Painter安装文件夹。
1. 在<b>backup\_libeay32.dll</b>中重命名文件<b>libeay32.dll</b>。
1. 下载以下文件： [已更新\_libeay32.zip](https://helpx.adobe.com/content/dam/help/en/substance-3d/documentation/spdoc/files/182266673/225968681/1/1644000679697/updated-libeay32.zip)。
1. 将dll文件从zip文件解压缩到安装文件夹（位于Substance Painter.exe文件旁边）。
1. 启动应用程序。
