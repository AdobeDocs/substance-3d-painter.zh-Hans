---
title: 夹持
description: 了解如何使用Substance 3D Painter的钳制滤镜。
source-git-commit: 644a36a1dde953c1d793821e104049ebb6ec3c19
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 2%
---

# 夹持

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![钳制图标](./Resources/icon_clamp.png "钳制")

<b>进入：</b>效果/调整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

钳制过滤器将值固定到定义的限制。

它可以直接用于填充图层上以限制材料的特定方面，或用于蒙版以将值限制在给定范围内。

</td>
</tr>
</table>

>[!NOTE]
>
> 当用于填充图层或作为颜色信息的通道时，夹具可单独影响每个颜色通道。 因此，如果给定像素的颜色为(R0， G 0.5， B 1.0)，且固定到0.5，则该像素的结果颜色将是(R 0， G 0.5， B 0.5)。 这是因为“蓝色”声道有足够高的值可被钳制，但其他声道没有。 这意味着钳制滤镜可以更改彩色内容的色相。
>
>如果不想修改色相，最好选择“色阶”等其他滤镜。

<a name="parameters"></a>

## 参数

| 参数名称 | 描述 |
| --- | --- |
| <b>分钟：</b> | 调整最小值。 |
| <b>最大值：</b> | 调整最大值。 |
