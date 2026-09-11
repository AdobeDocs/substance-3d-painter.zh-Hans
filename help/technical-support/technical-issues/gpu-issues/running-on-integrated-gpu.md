---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/technical-issues/gpu-issues/running-on-integrated-gpu.html"
breadcrumb-title: ''
description: 了解如何配置Substance 3D Painter以使用专用GPU而不是集成图形来获取更好的性能。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > GPU Issues > Running on integrated GPU
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 在集成的GPU上运行
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---


# 在集成的GPU上运行

![](../../../assets/integrated-gpu.png){width="500px"}

某些计算机可能默认设置为在集成芯片组而不是专用GPU上运行。\
由于集成芯片组上的性能非常低，我们建议改用专用GPU。 此时会显示弹出窗口并警告您相关信息。

如果使用NVIDIA GPU，请根据应用程序配置文件切换到NVIDIA GPU。 如果应用程序没有此类配置文件，您可以手动分配图形卡：

1. 右键单击桌面并选择“NVIDIA控制面板”**或**&#x200B;导航到“控制面板”并搜索“NVIDIA控制面板”
1. 在&#x200B;**3D设置**&#x200B;下，转到&#x200B;**管理3D设置**
1. 在&#x200B;**程序设置**&#x200B;选项卡下，为&#x200B;**Substance 3D Painter**&#x200B;添加新配置文件
1. 将首选图形处理器设置更改为高性能NVIDIA处理器
