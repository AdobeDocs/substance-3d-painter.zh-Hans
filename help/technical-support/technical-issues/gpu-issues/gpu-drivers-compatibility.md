---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/technical-issues/gpu-issues/gpu-drivers-compatibility.html"
breadcrumb-title: ''
description: 了解Substance 3D Painter的GPU驱动程序兼容性要求，以确保稳定的渲染和性能。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > GPU Issues > GPU drivers compatibility
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: GPU驱动程序兼容性
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---


# GPU驱动程序兼容性

本页将有关可能导致Substance 3D Painter出现问题的GPU驱动程序的信息重新分组。

## Nvidia

下表列出了已知可导致Nvidia GPU（GeForce或Quadro型号）出现问题的所有驱动程序版本：

| *驱动程序版本* | *问题描述* |
| --- | --- |
| <b> 425.xx </b> | GPU 射线追踪伪像。 |
| <b> 429.xx或更早版本</b> | 黑色纹理块伪像。 |
| <b> 435.xx或更早版本</b> | 计算纹理时出现sRGB颜色问题。 |
| <b> 439.xx </b> | 纹理腐败。 |
| <b> 441.08 </b> | 崩溃或稳定性问题。 |
| <b> 442.19 </b> | 崩溃或稳定性问题。 |
| <b>528.09</b> | 操作系统冻结。 |
| <b>572.16至572.42</b> | 烘焙纹理时出现伪影或崩溃。 |

### AMD

| *驱动程序版本* | *问题描述* |
| --- | --- |
| **20.7.x**&#x200B;至&#x200B;**20.11.2** | 纹理故障或损坏。 |
| **20.11.3**&#x200B;至&#x200B;**21.2.1** | 纹理故障或损坏以及崩溃或稳定性问题。 |
| **21.2.3**&#x200B;至&#x200B;**21.6.1** | 崩溃或稳定性问题。 |
