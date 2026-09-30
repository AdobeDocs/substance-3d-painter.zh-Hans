---
title: 灰度转换
description: 了解如何使用Substance 3D Painter的灰度转换滤镜。
source-git-commit: 644a36a1dde953c1d793821e104049ebb6ec3c19
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 4%
---

# 灰度转换

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![灰度转换图标](./Resources/icon_grayscale_conversion.png "灰度转换")

<b>进入：</b>效果/颜色，降低饱和度，最小值，最大值

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

灰度转换滤波器通过加权每个彩色通道的明亮度将通道/彩色图像转换为灰度。 有很多选项可以用来调整转换。

它用于纹理图层或蒙版图层，以将通道转换为灰度，或将彩色图像转换为灰度图像，然后将其用作蒙版。

</td>
</tr>
</table>

## 输入

| 输入名称 | 描述 |
| --- | --- |
| <b>自定义输入：</b>颜色 | 使用自定义纹理或锚点。 |

<a name="parameters"></a>

## 参数

| 参数名称 | 描述 |
| --- | --- |
| <b>频道输入：</b> | 选择用于转换的声道输入。 |
| <b>反转：</b> | 切换结果的反转。 |
| <b>余额：</b> | 调整黑白结果之间的平衡，类似于亮度调整。 |
| <b>对比度：</b> | 调整结果的对比度/衰减。 |
| <b>模式：</b> | 选择灰度转换模式。 |
| <b>红色：</b> | 调整红色通道的权重。 此权重用于计算灰度结果。 |
| <b>绿色：</b> | 调整绿色通道的权重。 此权重用于计算灰度结果。 |
| <b>蓝色：</b> | 调整蓝色通道的权重。 此权重用于计算灰度结果。 |
| <b>Alpha：</b> | 调整Alpha 通道的权重。 此权重用于计算灰度结果。 |

