---
title: 各向异性科威特语
description: 了解如何使用Substance 3D Painter各向异性科威特滤镜。
source-git-commit: 644a36a1dde953c1d793821e104049ebb6ec3c19
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 1%
---

# 各向异性科威特语

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![各向异性科威特图标](./Resources/icon_anisotropic_kuwahara.png "各向异性科威特图标")

<b>英寸：</b>效果/灰度，科威特，各向异性，风格化

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

各向异性Kuwahara滤波器在保留强方向性的同时产生绘画风格化效果。

它用于纹理图层或蒙版内（黑白输出），为完整的材料、噪声和蒙版创建风格化外观。

</td>
</tr>
</table>

## 输入

| 输入名称 | 描述 |
| --- | --- |
| <b>Radius映射：</b>灰度 | 使用自定义纹理或锚点。 |
| <b>自定义输入：</b>颜色 | 使用自定义纹理或锚点。 |

<a name="parameters"></a>

## 参数

| 参数名称 | 描述 |
| --- | --- |
| <b>提取方向：</b> | 选择滤镜如何推导模糊方向。 |
| <b>半径：</b> | 调整模糊半径。 值越高，模糊效果越强。 最大值为32。 |
| <b>Smoothness：</b> | 调整颜色沿计算方向混合的程度。 设置为0时，颜色大部分朝该方向移动，几乎没有混合。 |
| <b>锐度：</b> | 调整模糊区域的对比度，使其显得更平滑、定义更清晰。 |
| <b>张量Smoothness：</b> | 调整应用于根据图像计算并存储在方向图中的方向的模糊量。 当图像包含大量高频细节时，较高的值会产生更平滑的结果。 |
| <b>各向异性：</b> | 调整方向图对模糊的影响程度。 即使此值为0，方向图及其修饰符仍会影响结果，因为映射在Kuwahara滤镜内核中使用。 |
| <b>Anisotropy angle：</b> | 依次调整应用于方向图的旋转角度。 此旋转将添加到“Anisotropy angle映射”输入的值中。 |

