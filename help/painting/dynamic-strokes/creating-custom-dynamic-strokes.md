---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/painting/dynamic-strokes/creating-custom-dynamic-strokes.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中创建自定义动态笔触，以设计独特的画笔描边行为和效果。
helpx_creative_field: ""
helpx_description: Painter > Painting > Dynamic strokes > Creating Custom Dynamic Strokes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 创建自定义动态笔触
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---


# 创建自定义动态笔触

要创建自定义动态笔触，可以使用两个选项：

* 使用现有Substance资源创建新的画笔/工具预设
* 从头开始创建新的Substance资源（需要[Substance 3D Designer](https://substance3d.adobe.com/display/SDDOC/Substance+Designer) ）。

此外，还建议您在创建自定义Substance文件之前阅读[动态描边性能](dynamic-stroke-performances.md)，以避免出现任何问题。

## 重新使用现有资源

从头开始创建新动态笔触可能很困难。 不妨先使用现有资源、微调这些资源，然后将其另存为新预设。

在Shelf中查找适合您需求的兼容资源，然后查看我们的页面以了解[预设](../presets/presets.md)。

## 为动态笔触创建自定义Substance文件

以下是Substance图中支持动态笔触的参数列表。

| 变量标识符 | 描述 |
| --- | --- |
| <b>随机植入</b> | 如果Substance文件在展现随机种子的情况下经过烹饪，则将可使用“动态描边”功能对其进行控制。 |
| <b>stampIndex</b> | 绘画画笔描边时，Substance 3D Painter将提供<b>Integer1</b>。 最小值和最大值无效，Substance 3D Painter将忽略它们。 |
| <b>stampCycleCount</b> | <b>Integer1</b> Painter将读取参数默认值、最小值和最大值，以显示图章周期计数参数。 此参数控制将创建多少个唯一的Substance变化。 |
| <b>$time</b> | <b>浮点1</b>在根据已用绘制时间（每个描边）绘制画笔描边时，将由Substance 3D Painter馈送。 该特性会产生许多Substance变化，从而影响性能。 |
| <b>描边间距</b> | <b>float1</b>绘制的整个描边的当前间距值。 |
| <b>描边大小</b> | <b>float1</b>绘制的整个描边的当前大小值。 |
| <b>stampStrokePosition</b> | <b>integer1</b>用于指定描边的开始/开始。 结束值仅在路径描边上可用，而不通过手动绘画。 可能的值：<ul data-preserve-html="true"> <li data-preserve-html="true">0 =中间</li> <li data-preserve-html="true">1 =开始</li> <li data-preserve-html="true">2 =结束</li> </ul>可以使用isstrokepositionactive user标记禁用。 |
| <b>distanceAlongCurve</b> | <b>float1</b>给定图章沿路径的当前距离。 该特性会产生许多Substance变化，从而影响性能。 可以使用<b>iscurvedistanceactive</b>用户标记禁用。 |
| <b>distanceMaxCurve</b> | <b>float1</b>使用路径工具创建的路径的总长度。 可以使用<b>iscurvedistanceactive</b>用户标记禁用。 |
| <b>pathCorner</b> | <b>integer1</b>指示功能区使用的边角类型。 可能的值：<ul data-preserve-html="true"> <li data-preserve-html="true">0 =无角</li> <li data-preserve-html="true">1 =左角</li> <li data-preserve-html="true">2 =右角</li> </ul> |
| <b>pathCornerAngle</b> | 功能区路径上角的<b>浮动</b>角度（以弧度为单位）。 可用于根据精确的角度值补偿或调整角落的外观。 |
| <b>patchLengthOnCurve</b> | 功能区路径上的节（修补程序）的<b>浮动</b>大小。 结合<b>distanceAlongCurve</b>和<b>distanceMaxCurve</b>，可用于规范化修补的大小。 |
