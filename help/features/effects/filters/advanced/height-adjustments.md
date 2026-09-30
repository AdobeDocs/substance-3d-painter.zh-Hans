---
title: Height调整
description: 了解如何使用Substance 3D Painter的Height调整滤镜。
source-git-commit: 644a36a1dde953c1d793821e104049ebb6ec3c19
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 1%
---

# Height调整

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Height调整图标](./Resources/icon_height_adjust.png "Height调整")

<b>入：</b>效果/调整、缩放、偏移、反转

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

“Height调整”滤镜将Height声道反相、偏移或乘以所选值。

该功能可在纹理图层上或蒙版内（黑白输出）使用，以非破坏性方式调整Height信息。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

| 参数名称 | 描述 |
| --- | --- |
| <b>反转：</b> | 切换结果的反转。 |
| <b>偏移：</b> | 通过相加或相减指定量来调整Height值。 |
| <b>乘：</b> | 将Height值与此值相乘。 作为乘数，这会使较高的区域较高，较低的区域较低。 |

>[!NOTE]
>
> 首先应用偏移的&#x200B;**乘**&#x200B;和&#x200B;**偏移**&#x200B;参数堆叠。 如果在给定点偏移导致Height值为零，则乘法将乘以0，这意味着它将在该点不导致任何更改。 要乘以然后偏移乘以的值，可以添加第二个“Height调整”滤镜。
