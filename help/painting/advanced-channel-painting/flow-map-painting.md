---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/painting/advanced-channel-painting/flow-map-painting.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中绘制流图以控制材料流方向和各向异性效果。
helpx_creative_field: ""
helpx_description: Painter > Painting > Advanced channel painting > Flow Map Painting
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 流程图绘画
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---


# 流程图绘画

虽然规划了专用通道，但同时使用“正常”通道和一些画笔参数，可以绘制Substance 3D Painter中的流图。

## 第1步：创建法线图

创建16 x 16像素的法线映射纹理。 颜色必须为128、255、128，这应提供以下颜色： ![](../../assets/up-dx.png)\
（此颜色等效于在DirectX中查找的矢量）

## 第2步：添加普通通道

在您的Substance 3D Painter项目中，如果&#x200B;**普通**&#x200B;频道尚不存在，请通过&#x200B;**纹理集设置**&#x200B;来添加此频道。

## 第3步：画笔设置

在画笔参数中启用跟随路径功能。 将法线映射纹理（步骤1）加载到法线通道槽中。 禁用其他通道。

![](../../assets/brush-settings-1.png){width="300px"}

## 第4步：绘制！

通过在启用“跟随路径”设置的网格上绘画，画笔描边会将方向绘制到法线图中。

![](../../assets/painting-1.png){width="700px"}
