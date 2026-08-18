---
title: UV随机颜色
description: 了解如何使用Substance 3D Painter的UV随机颜色生成器。
source-git-commit: b7770a9497f0db047433aec32c31b57f8dc13ae7
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---


# UV随机颜色

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../../assets/generators/icon_uv_random_color.png" alt=""/><br><strong>在：</strong>实用程序中，蒙版</td>
    <td style="border: 0;" valign="top"><strong>说明</strong><br>UV随机颜色生成器会为每个UV 岛分配纯的独特颜色。 这通常可用作具有复杂网格的诊断工具。<br><br>UV随机颜色可用于创建蒙版（黑白输出），或直接用作填充图层以根据UV 岛将颜色变化应用于网格，例如，将木地板的每个平板随机化。</td>
  </tr>
</table>

## 输入

| 输入名称 | 描述 |
| --- | --- |
| **自定义渐变** | 使用“渐变”映射定义颜色范围。 |

## 参数

<table>
  <tr>
    <th>参数名称</th>
    <th>描述</th>
  </tr>
  <tr>
    <td><strong>Seed</strong></td>
    <td>设置用于生成Dirt纹理的种子值。 <br><ul><li>单击“随机”可切换到另一个随机植入。</li><li>单击铅笔以查看当前种子值，并根据需要输入特定值。</li></ul></td>
  </tr>
  <tr>
    <td><strong>颜色源模式</strong></td>
    <td>确定使用的颜色源模式。 <br><ul><li><strong>随机</strong>：在随机模式下，将定义并随机分配颜色。</li><li><strong>自定义渐变</strong>：在自定义渐变模式中，您有一个额外的输入来添加一个自定义渐变映射，颜色将从该映射中选取。</li></ul></td>
  </tr>
</table>
