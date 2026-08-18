---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/technical-issues/gpu-issues/forcing-the-external-gpu-on-mac-os.html"
breadcrumb-title: ''
description: 了解如何强制Substance 3D Painter在macOS上使用外部GPU以提高渲染性能。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > GPU Issues > Forcing the external GPU on Mac OS
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 在Mac操作系统上强制使用外部GPU
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---


# 在Mac操作系统上强制使用外部GPU

在Mac OS Mojave上，可以指定每个应用程序使用外部GPU。 启用此设置后，Substance 3D Painter的性能和稳定性可能会有所改善。

有关详细信息，请参阅[Apple文档](https://support.apple.com/en-us/HT208544)。

要启用它，请执行以下操作：

1. 如果Substance 3D Painter已在运行，请将其关闭。
1. 在访达中选择Substance 3D Painter，您可以在&#x200B;**Applications**&#x200B;文件夹中找到它**.**
1. 按&#x200B;**Command-I**&#x200B;或右键单击&#x200B;**Substance 3D Painter**&#x200B;应用程序，然后选择&#x200B;**获取信息**。
1. 在新窗口中，启用设置&#x200B;**首选外部GPU**。
1. 重新启动Substance 3D Painter。

>[!NOTE]
>
> 如果未连接eGPU或MacOS的当前版本太旧，则此设置将不可见。
