---
title: PBR 验证
description: 了解如何使用Substance 3D Painter的PBR 验证滤镜。
source-git-commit: 644a36a1dde953c1d793821e104049ebb6ec3c19
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 2%
---

# PBR 验证

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![PBR 验证图标](./Resources/icon_pbr_validate.png "PBR 验证")

<b>范围：</b>效果/pbr，金属，粗糙度

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

该PBR 验证滤波器通过检查反照率暗值和金属反射率范围来验证PBR数据。

它用于填充图层以验证材料值是否保持在预期的PBR范围内。 导出材料时不应启用PBR 验证。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

| 参数名称 | 描述 |
| --- | --- |
| <b>验证模式：</b> | 选择是验证反照率、金属反射率，还是同时验证两者。 |
| <b>反照率的深色范围阈值：</b> | 为反照率验证选择允许的最小深色值阈值。 |
| <b>金属反射范围：</b> | 选择用于验证金属值的反射率范围。 |
| <b>叠加图：</b> | 在地图数据上切换验证叠加。 |

