---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/pipeline-and-integration/configuration/remote-desktop.html"
breadcrumb-title: ''
description: 了解如何配置Substance 3D Painter以进行远程桌面访问，以启用远程工作流程和协作。
helpx_creative_field: ""
helpx_description: Painter > Pipeline and integration > Configuration > Remote Desktop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 远程桌面
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---


# 远程桌面

本页介绍使Substance 3D Painter能够在Windows上通过远程桌面(RDP)运行的解决方案和替代方法。

默认情况下，Windows上的RDP在不存在或过低的OpenGL上下文中运行，这会导致应用程序无法正常工作或崩溃。 Substance 3D Painter需要OpenGL 3.3上下文。 以下是缓解此问题的解决方案，但没有可用的保证，因为初始问题依赖于Windows和某些GPU驱动程序。

>[!NOTE]
>
> 默认情况下，Nvidia Quadro GPU可以在RDP模式下运行应用程序，而Nvidia GeForce GPU仅提供OpenGL 1.4上下文（对于Substance 3D Painter来说太低）。 可以安装一个可执行文件来对此进行补救，请参阅： <https://developer.nvidia.com/designworks>

## Windows策略配置

在Windows 10上，可能需要更改&#x200B;**组策略**&#x200B;以允许在RDP模式下运行GPU。

具体操作如下：

1. 按&#x200B;**Win + R**&#x200B;打开执行窗口
1. 键入“ **gpedit.msc**”，然后输入
1. 导航到&#x200B;**本地计算机策略\计算机配置\管理模板\Windows组件\远程桌面服务\远程桌面会话主机\远程会话环境**
1. 启用选项&#x200B;**对所有远程桌面服务会话使用硬件默认图形适配器** 。

## Windows TSCON命令

如果以前的策略更改不起作用，则可以尝试使用&#x200B;**tscon**&#x200B;命令行。 此命令断开远程计算机的连接，并将新计算机连接到物理硬件（鼠标、键盘等）。 然后，只需运行应用程序并重新进行远程连接，即可在GPU上使用该应用程序。

1. 按键&#x200B;**Windows+R**&#x200B;打开&#x200B;**执行**&#x200B;窗口。
1. 键入&#x200B;**cmd**&#x200B;并按&#x200B;**Enter** 。
1. 在命令行类型和以下命令中： **tscon 1 /dest:console**
1. 按Enter
1. 在命令行中键入下一个命令： **启动“Path/To/Substance/Painter/Folder/Substance 3D Painter.exe”** （确保更改路径以匹配计算机）
1. 按Enter

完成这些步骤后，请等待几秒钟让应用程序启动，然后重新连接到您的会话。

如果此过程不起作用，则可能需要在管理员模式下运行Windows命令行。

## 替代项

如果先前的建议仍然不起作用，我们建议使用替代解决方案，例如VNC或Teamviewer，它们通过远程连接支持GPU。
