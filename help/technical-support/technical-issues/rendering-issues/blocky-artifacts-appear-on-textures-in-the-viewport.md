---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/technical-support/technical-issues/rendering-issues/blocky-artifacts-appear-on-textures-in-the-viewport.html"
breadcrumb-title: ''
description: 了解如何修复Substance 3D Painter视口中纹理上出现的块状伪影，以实现干净的视觉品质。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > Rendering Issues > Blocky artifacts appear on textures in the viewport
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 视区的纹理上出现块状伪像
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---


# 视区的纹理上出现块状伪像

从版本2018.3.0开始，视区中可能会显示以下种类的对象：

![](../../../assets/viewport-artifacts.jpg){width="400px"}

这些伪影与Nvidia GPU驱动程序的问题有关。\
为了避免伪影，需要取消稀疏虚拟纹理硬件支持。

GeForce **驱动程序440.97**&#x200B;现在&#x200B;**已修复此问题** 。 我们建议更新这些驱动程序并保持SVT处于启用状态，以获得良好的性能。

Nvidia网站<https://www.nvidia.com/Download/index.aspx>上提供了新的驱动程序

## 禁用稀疏虚拟纹理硬件加速

### 1 — 启动Substance 3D Painter并打开设置

![](../../../assets/settings-34.png)

通过“编辑”>“设置”打开主要设置。

### 2 — 查找名为“稀疏虚拟纹理”的部分

![](../../../assets/svt-subsection.png)

在“常规”部分内，向下滚动并找到名为“稀疏虚拟纹理”的子部分

### 3 — 取消选中设置

![](../../../assets/uncheck-hardware.png)

取消选中“硬件支持加速”设置，将其禁用。

### 4 — 验证并重新启动Substance 3D Painter

![](../../../assets/validate-1.png)

单击“OK”（确定）按钮验证更改。

![](../../../assets/restart-3.png)

单击“是”按钮重新启动Substance 3D Painter以应用更改。
