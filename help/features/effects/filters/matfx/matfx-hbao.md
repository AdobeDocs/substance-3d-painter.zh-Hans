---
title: MatFX HBAO
description: 了解如何使用Substance 3D Painter的MatFX HBAO滤镜。
source-git-commit: 644a36a1dde953c1d793821e104049ebb6ec3c19
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 2%
---

# MatFX HBAO

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![MatFX HBAO图标](./Resources/icon_matfx_hbao.png "MatFX HBAO")

<b>范围：</b>效果/ambient occlusion、Height、着色

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 描述

MatFX HBAO滤镜根据Height信息生成基于水平的ambient occlusion。

它用于纹理图层或蒙版，以根据源通道或Height信息添加深度并接触阴影。

</td>
</tr>
</table>

<a name="parameters"></a>

## 参数

| 参数名称 | 描述 |
| --- | --- |
| <b>模糊强度：</b> | 调整结果的模糊强度。 |
| <b>模糊绕排：</b> | 切换模糊包装。 启用后，此效果将从纹理的另一侧对像素进行取样。 |
| <b>频道源：</b> | 选择用于生成遮蔽的声道源。 |
| <b>使用世界单位：</b> | 切换使用世界空间单位。 |
| <b>深度：</b> | 调整Height输入的感知深度。 |
| <b>半径：</b> | 调整遮蔽效果的采样半径。 |
| <b>强度：</b> | 调整遮蔽的强度。 |
| <b>浮雕平衡：</b> | 调整浮雕贡献的余额。 |
