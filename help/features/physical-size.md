---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/features/physical-size.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中设置物理尺寸，以定义实际尺寸进行准确的纹理缩放。
helpx_creative_field: ""
helpx_description: Painter > Features > Physical size
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 实际大小
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 2%

---


# 实际大小

![](../assets/banner-physicalsize-2.png)

物理尺寸是Substance材料中的属性，用于定义文档的实际大小。 它可用于精确匹配3D曲面上材料的大小和外观。 Painter使用厘米作为默认的内部单位。

要使用物理尺寸，请应用具有此材料且值不是0,0，0的属性，然后在“UV变换”>“缩放”下启用“填充图层（或效果）”中的物理尺寸模式。

有关更多信息，请参阅：

* [填充投影](../painting/fill-projections/fill-projections.md)中的<b>物理尺寸</b>参数
* [视口设置](../interface/display-settings/viewport-settings.md)中的<b>网格</b>参数
* <b>基于[着色器设置](../interface/shader-settings/shader-settings.md)中的物理尺寸</b>位移

>[!NOTE]
>
> * 从Painter版本8.3开始，物理尺寸功能适用于所有类型的投影。
> * 大多数网格文件格式都会指定在创建网格时使用的单位，此单位将在导入时自动转换为厘米。
> * 某些格式(如.obj)没有单位信息，因此使用.obj网格创建项目时，默认情况下将使用公分进行测量，而不进行任何转换。
