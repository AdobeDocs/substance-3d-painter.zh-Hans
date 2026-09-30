---
title: MatFX边缘损坏
description: 了解如何使用Substance 3D Painter的“MatFX边缘损坏”滤镜。
source-git-commit: 644a36a1dde953c1d793821e104049ebb6ec3c19
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 1%
---

# MatFX边缘损坏

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![MatFX边缘损坏图标](./Resources/icon_matfx_edge_damages.png "MatFX边缘损坏")

<b>进入：</b>效果/模糊，灰度

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

“MatFX Edge Impaints”（MatFX边缘损坏）滤镜创建有碎片和损坏的边缘细节。 边缘损坏与MatFX细节Edge Wear滤镜的行为不同，因为边缘损坏不会更改损坏区域的颜色。 这意味着它对于模拟塑料或树脂等材料的损伤更为有用，而不是对Edge Wear有用，后者更适合用于喷涂金属等材料。

在纹理图层或材料堆叠上使用“MatFX边缘损坏”可添加磨损、划痕和损坏的边缘细节。

</td>
</tr>
</table>

>[!NOTE]
>
> 为了使MatFX Edge Impaints滤镜修改Height通道，通道中需要存在Height数据。 换句话说，如果滤镜图层下方没有包含Height数据的图层，则滤镜将对Height声道没有明显的影响。

<a name="parameters"></a>

## 参数

| 参数名称 | 描述 |
| --- | --- |
| <b>模糊强度：</b> | 调整模糊效果的强度。 |
| <b>模糊绕排：</b> | 切换模糊包装。 启用后，此效果将从纹理的另一侧对像素进行取样。 |
| <b>级别：</b> | 调整整体损坏程度。 |
| <b>对比度：</b> | 调整结果的对比度或衰减。 |
| <b>Scratches强度：</b> | 调整划痕的强度。 |
| <b>损坏粗糙度：</b> | 调整损坏区域的粗糙度。 |
| <b>损坏深度：</b> | 调整损坏区域的深度。 |
