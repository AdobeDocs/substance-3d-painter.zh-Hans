---
title: 填充区域蒙版
description: 了解如何使用Substance 3D Painter的填充区域蒙版滤镜。
source-git-commit: 644a36a1dde953c1d793821e104049ebb6ec3c19
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 2%
---

# 填充区域蒙版

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![填充区域蒙版图标](./Resources/icon_fill_area_mask.png "填充区域蒙版")

<b>范围：</b>效果/填充、形状、轮廓、灰度

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

“填充区域蒙版”滤镜将轮廓转换为填充形状。 任何具有连续边框的区域都会被填充。

添加绘画图层后，它用于蒙版（黑白输出）图层以填充闭合的绘制描边。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

| 参数名称 | 描述 |
| --- | --- |
| <b>区域检测：</b> | 选择如何识别要填充的区域。 |
| <b>区域检测阈值：</b> | 调整区域检测阈值。 |
| <b>调试区域检测：</b> | 切换区域检测设置检测到的轮廓的显示。 这有助于确定可能未完全闭合的区域。 |
| <b>UV边框行为：</b> | 选择如何在区域填充期间处理UV边界。 |
| <b>UV边界检测阈值：</b> | 调整用于忽略UV区域的阈值，否则这些区域将由区域检测过程填充。 |
