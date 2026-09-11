---
title: 三平面高级
description: 了解如何使用Substance 3D Painter的三平面高级生成器。
source-git-commit: b7770a9497f0db047433aec32c31b57f8dc13ae7
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 2%

---


# 三平面高级

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../../assets/generators/icon_tri_planar_advanced.png" alt=""/><br><strong>进入：</strong>蒙版，生成器</td>
    <td style="border: 0;" valign="top"><strong>说明</strong><br>三平面高级生成器是三平面混合模式的独立版本，可手动控制整个投影，包括控制每个单独轴的所有旋转和偏移值。 与原始填充投影相比，Tri-平面 Advanced生成器使用世界空间法线来混合3个投影轴，而原始实现仅依赖于低多边形几何。 这样会产生更进行控制，且结果更准确。<br><br>三平面高级生成器输出单色（黑白）纹理。 因此，对于生成用作蒙版的自定义蒙版或锚点的三平面混合非常有用。需要<br><br>烘焙的位置和世界空间法线映射作为图像输入。 <a href="../../../baking/baking.md">在此详细了解烘焙</a>。</td>
  </tr>
</table>

## 输入

| 输入名称 | 描述 |
| --- | --- |
| **世界空间法线**&#x200B;颜色 | 使用烘焙的世界空间法线映射。 |
| **位置**&#x200B;颜色 | 使用烘焙的位置图。 |
| **蒙版**&#x200B;灰度 | 使用自定义纹理或锚点。 |

## 参数

<table>
  <tr>
    <th>参数名称</th>
    <th>描述</th>
  </tr>
  <tr>
    <td><strong>投影</strong></td>
    <td>选择是投影所有轴，还是仅投影单个轴。</td>
  </tr>
  <tr>
    <td><strong>混合模式</strong></td>
    <td>选择混合模式以跨轴混合。<br><ul><li><strong>线性</strong>：在线性混合模式下，混合过渡线是直的。</li><li><strong>高级</strong>：在“高级”混合模式下，根据3个轴之间的最大值和给定位置的法线角度来混合轴。</li></ul></td>
  </tr>
  <tr>
    <td><strong>混合对比度</strong></td>
    <td>调整混合过渡线变得模糊的程度。</td>
  </tr>
  <tr>
    <td><strong>拼贴</strong></td>
    <td>调整蒙版纹理的拼贴。</td>
  </tr>
</table>

### 轴X

| 参数名称 | 描述 |
| --- | --- |
| **旋转X** | 旋转X纹理投影。 |
| **偏移X X** | 左右移动X纹理投影。 |
| **偏移X Y** | 向上或向下移动“X轴”纹理投影。 |

### 轴Y

| 参数名称 | 描述 |
| --- | --- |
| **旋转X** | 旋转Y纹理投影。 |
| **偏移Y X** | 向左或向右移动Y纹理投影。 |
| **偏移Y** | 向上或向下移动Y轴纹理投影。 |

### Z轴

| 参数名称 | 描述 |
| --- | --- |
| **旋转X** | 旋转Z轴纹理投影。 |
| **偏移Z X** | 向左或向右移动Z轴纹理投影。 |
| **偏移Z Y** | 上下移动Z纹理投影。 |
