---
title: 3D距离
description: 了解如何使用Substance 3D Painter的3D距离生成器。
source-git-commit: b095b9b437f75bbb3a3b85ee84a6850026c3bf98
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 1%

---


# 3D距离

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../../assets/generators/icon_3d_distance.webp" alt=""/><br><strong>进入：</strong>蒙版，生成器</td>
    <td style="border: 0;" valign="top"><strong>描述</strong><br>3D距离生成器在3D空间中定义一个点（源点），并使用单色渐变显示与该点的距离。 网格曲面上靠近点的区域较暗，远处的区域较亮（默认情况下）。<br><br>需要烘焙位置图作为图像输入。 <a href="../../../baking/baking.md">在此处了解有关烘焙的更多信息</a>。<br><br>3D距离输出单色（黑白）纹理。 因此，它对于生成可创建远离给定位置的渐变的蒙版非常有用。<br><br></td>
  </tr>
</table>

## 输入

| 输入名称 | 描述 |
| --- | --- |
| **位置** | 使用烘焙的位置图计算距离。 |

## 参数

| 参数名称 | 描述 |
| --- | --- |
| **反转** | 反转渐变。 |
| **位置X** | 沿x轴变换源点。 |
| **位置Y** | 沿y轴变换源点。 |
| **位置Z** | 沿z轴变换源点。 |
| **半径** | 调整距离衰减的大小。 |
| **偏移** | 将渐变的开始和结束位置移向或移离源点。 远离源点（增加偏移）会导致源点附近的较暗区域较大。 向源点附近移动可使渐变变亮，如果&#x200B;**偏移**&#x200B;设置为0，则可能会将其全部移除。 |
| **对比度** | 调整球面渐变的对比度。 |
