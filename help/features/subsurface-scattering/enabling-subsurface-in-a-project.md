---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/features/subsurface-scattering/enabling-subsurface-in-a-project.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter项目中启用子表面散射，以创建逼真的半透明素材效果。
helpx_creative_field: ""
helpx_description: Painter > Features > Subsurface Scattering > Enabling Subsurface in a Project
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 在项目中启用子曲面
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---


# 在项目中启用子曲面

为了在Substance 3D Painter中正确激活次表面散射，首先需要设置几个参数。\
本页提供了有关要启用哪些参数的指南。

## 1 — 纹理集设置

在[纹理集](../../interface/texture-set/texture-set.md)中，添加&#x200B;**散射**&#x200B;通道（如果尚未存在）：

![](../../assets/add-channel.png)

>[!NOTE]
>
> 散射通道的工作方式类似于&#x200B;**表面**&#x200B;上的&#x200B;**蒙版**：如果通道为黑色，则根本没有次表面，而如果通道为白色，则次表面强度将达到最大。 此通道是灰度值，默认情况下为&#x200B;**黑色** 。 在图层栈栈中添加填充图层以控制默认颜色，或使用绘画图层手动控制强度。

## 2 — 全局子表面设置

在[显示设置](../../interface/display-settings/display-settings.md)（在“后效果”设置下方）中启用主要“子表面散射”设置：

![](../../assets/enable-subsurface.png)

>[!NOTE]
>
> 启用/禁用子表面效果会影响整个项目。 如果全局参数太重，则使用全局参数会有所帮助。

## 3 — 着色器设置

![](../../assets/shader-parameters.png)

在带有默认着色器的[着色器设置](../../interface/shader-settings/shader-settings.md)窗口中，可以找到具有两个设置的“**SSS参数**”组。\
更改比例和颜色以适应目标素材。 有关这些设置的更多详细信息，请参阅： [子表面参数](subsurface-parameters.md)

## 福利：启用阴影

次表面散射效果很好，但单独使用时可能看起来很奇怪。\
启用阴影有助于改善视区的最终观感，并改善最终素材的真实感。

在[环境设置](../../interface/display-settings/environment-settings.md)窗口中，启用“**阴影**”设置：

![](../../assets/shadow-2.png)
