---
title: 量化
description: 了解如何使用Substance 3D Painter的Quantize滤镜。
source-git-commit: 644a36a1dde953c1d793821e104049ebb6ec3c19
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 1%
---

# 量化

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Quantize图标](./Resources/icon_quantize.png "Quantize")

<b>进入：</b>效果/量化，颜色

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

“量化”滤镜将图像缩小为一组有限的颜色。

它用于纹理图层以创建扁平的、色调分离的或风格化的颜色区域。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

| 参数名称 | 描述 |
| --- | --- |
| <b>颜色量：</b> | 调整量化图像中使用的最大颜色数。 该值还驱动提取的调色板，但实际计数可能更低，具体取决于量化方法。 检查“调色板颜色量”输出以查看所提取颜色的最终数量。 |
| <b>轮廓平滑：</b> | 调整应用于输入图像的平滑半径，将量化结果简化为更坚实、更有凝聚力的形状。 较高的值会显着增加计算时间。 |
| <b>仿色：</b> | 调整用于重新创建渐变和颜色混合的仿色量，同时仍仅使用量化后剩余的颜色。 将“等高线平滑”值设置为0作为预期的仿色效果。 |
| <b>仿色模式：</b> | 选择用于在原始图像中重新创建渐变和颜色混合的仿色图案。 |
| <b>距离色彩空间：</b> | 选择用于在量化期间比较和分布颜色的色彩空间。 对可感知实验室图像使用“颜色”(Color)，对原始数据（如法线图）使用“RGB”(Data)。 |
| <b>应用于Alpha：</b> | 切换图层Alpha 通道的量化。 |
| <b>Alpha阈值：</b> | 调整Alpha阈值。 |

