---
breadcrumb-title: ""
description: 了解如何修复视口中显示在纹理上的块状伪影，以实现干净的视觉质量。
title: 视口中的纹理上出现块状伪像
user-guide-description: ""
user-guide-title: ""
source-git-commit: 6b6d52207ca1d043aaa1b2b14145b6b49d4c1942
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%
---

# 视口中的纹理上出现块状伪像

从版本2018.3.0开始，视口中可能会出现以下种类的伪像：

![](../../../assets/viewport-artifacts.jpg){width="400px"}

这些伪影与Nvidia GPU驱动程序的问题有关。\
为了避免出现伪影，需要停用Sparse Virtual Texture硬件支持。

GeForce **驱动程序440.97**&#x200B;现在&#x200B;**已修复此问题** 。 我们建议更新这些驱动程序并保持SVT处于启用状态，以获得良好的性能。

Nvidia网站<https://www.nvidia.com/Download/index.aspx>上提供了新的驱动程序

## 禁用Sparse Virtual Texture硬件加速

### 1 — 启动Substance 3D Painter并打开设置

![](../../../assets/settings-34.png)

通过“编辑”>“设置”打开主要设置。

### 2 — 查找名为“Sparse Virtual Texture”的部分

![](../../../assets/svt-subsection.png)

在“常规”部分中，向下滚动并找到名为“Sparse Virtual Texture”的子部分

### 3 — 取消选中设置

![](../../../assets/uncheck-hardware.png)

取消选中“硬件支持加速”设置，将其禁用。

### 4 — 验证并重新启动Substance 3D Painter

![](../../../assets/validate-1.png)

单击“OK”（确定）按钮验证更改。

![](../../../assets/restart-3.png)

单击“是”按钮重新启动Substance 3D Painter以应用更改。
