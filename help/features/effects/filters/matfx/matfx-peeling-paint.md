---
title: MatFX剥落绘画
description: 了解如何使用Substance 3D Painter的MatFX剥落绘画滤镜。
source-git-commit: 644a36a1dde953c1d793821e104049ebb6ec3c19
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 2%
---

# MatFX剥落绘画

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![MatFX剥落绘画图标](./Resources/icon_matfx_peeling_paint.png "MatFX剥落绘画")

<b>进入：</b>效果/模糊，灰度

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

MatFX剥落绘画滤镜可产生薄片和剥落绘画效果。

它可以用于纹理图层或材料堆叠，以模拟剥落绘画、脱落的涂层和公开底层材料。

</td>
</tr>
</table>

>[!NOTE]
>
> 要公开基础材料，请在组中使用MatFX剥离绘画。 图层堆叠中位于组外部和组下方的图层将公开已剥离绘画拉离表面的位置。

<a name="parameters"></a>

## 参数

| 参数名称 | 描述 |
| --- | --- |
| <b>模糊强度：</b> | 调整模糊效果的强度。 |
| <b>模糊绕排：</b> | 切换模糊包装。 启用后，此效果将从纹理的另一侧对像素进行取样。 |
| <b>剥离级别：</b> | 调整整体剥落程度。 |
| <b>剥离距离：</b> | 调整绘画脱落的距离。 |
| <b>薄片级别：</b> | 调整剥落的量。 |
| <b>气泡密度：</b> | 调整气泡的密度。 |
| <b>薄片密度：</b> | 调整薄片的密度。 |
| <b>薄片X数量：</b> | 调整沿X轴的剥落量。 |
| <b>薄片Y数量：</b> | 调整Y轴上的薄片数量。 |
| <b>使用弯曲：</b> | 切换对弯曲输入的使用。 |
| <b>弯曲距离：</b> | 调整弯曲采样距离。 |
| <b>弯曲对比度：</b> | 调整弯曲输入的对比度。 |

### 技术参数

这些参数允许您修改剥离材料的顶部曲面。

| 参数名称 | 描述 |
| --- | --- |
| <b>明度：</b> | 调整明度。 |
| <b>对比度：</b> | 调整结果的对比度或衰减。 |
| <b>色相转换：</b> | 调整色相偏移。 |
| <b>饱和度：</b> | 调整饱和度。 |
| <b>正常强度：</b> | 调整正常强度。 |
| <b>Height范围：</b> | 调整效果使用的Height范围。 |
| <b>Height位置：</b> | 调整效果使用的Height位置。 |
| <b>Ambient occlusion强度：</b> | 调整ambient occlusion的强度。 |
