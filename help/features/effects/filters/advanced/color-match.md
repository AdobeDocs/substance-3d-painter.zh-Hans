---
title: 颜色匹配
description: 了解如何在Substance 3D Painter中使用“颜色匹配”滤镜。
source-git-commit: 644a36a1dde953c1d793821e104049ebb6ec3c19
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 1%
---

# 颜色匹配

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="./Resources/icon_color_match.png" alt="“颜色匹配”图标" title="颜色匹配"/><br><strong>进入：</strong>效果/调整</td>
    <td style="border: 0;" valign="top">说明<br>颜色匹配筛选器将定义的源颜色范围与目标颜色范围匹配，并且支持输入槽来定义源值和目标值。 “颜色匹配”允许您在更改表面的颜色时保持细节，并控制如何处理色相、色度和亮度。在填充图层上使用“<br>颜色匹配”进行细微的颜色调整。</td>
  </tr>
</table>

## 输入

| 输入名称 | 描述 |
| --- | --- |
| **源颜色：** | 源颜色的输入插槽。 使用自定义颜色映射或锚点。 |
| **目标颜色：** | 目标颜色的输入插槽。 使用自定义颜色映射或锚点。 |

## 参数

<table>
  <tr>
    <th>参数名称</th>
    <th>描述</th>
  </tr>
  <tr>
    <td><strong>源颜色模式：</strong></td>
    <td>选择源颜色的源。<br><ul><li><strong>平均</strong>：使用现有材料颜色作为源颜色。 注意，这需要将图层混合模式设置为<strong>通过</strong>。</li><li><strong>参数</strong>：使用参数设置源颜色。</li><li><strong>输入</strong>：使用图像输入设置源颜色。</li></ul></td>
  </tr>
  <tr>
    <td><strong>源颜色：</strong></td>
    <td>在<strong>源颜色模式</strong>设置为<strong>参数</strong>时调整源颜色。</td>
  </tr>
  <tr>
    <td><strong>目标颜色模式：</strong></td>
    <td>选择目标颜色的源。<br><ul><li><strong>参数</strong>：使用参数设置目标颜色。</li><li><strong>输入</strong>：使用图像输入设置目标颜色。</li></ul></td>
  </tr>
  <tr>
    <td><strong>目标颜色：</strong></td>
    <td>在<strong>目标颜色模式</strong>设置为<strong>参数</strong>时调整目标颜色。</td>
  </tr>
  <tr>
    <td><strong>自定颜色变化：</strong></td>
    <td>切换自定义色相、色度和亮度变量控件。</td>
  </tr>
  <tr>
    <td><strong>色相：</strong></td>
    <td>调整应用于结果的色相变化。</td>
  </tr>
  <tr>
    <td><strong>色度：</strong></td>
    <td>调整应用于结果的色度变化。</td>
  </tr>
  <tr>
    <td><strong>亮度：</strong></td>
    <td>调整应用于结果的亮度变化。</td>
  </tr>
</table>