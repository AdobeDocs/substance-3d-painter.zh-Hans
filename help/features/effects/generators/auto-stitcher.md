---
title: 自动拼接器
description: 了解如何使用Substance 3D Painter的自动缝合器生成器。
source-git-commit: b095b9b437f75bbb3a3b85ee84a6850026c3bf98
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 1%

---


# 自动拼接器

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../../assets/generators/icon_auto_stitcher.png" alt=""/><br><strong>进入：</strong>缝合，缝合</td>
    <td style="border: 0;" valign="top"><strong>说明</strong><br>自动缝合器生成器会自动沿程序生成的路径创建缝合效果。 可以基于接缝、弯曲或自定义输入图生成这些路径。<br><br>自动缝合器生成器输出单色（黑白）纹理。 因此，它对于生成蒙版以应用拼接效果非常有用。<br><br>要使用弯曲蒙版模式，需要烘焙弯曲图。 <a href="../../../baking/baking.md">在此详细了解烘焙</a>。</td>
  </tr>
</table>

## 输入

<table>
  <tr>
    <th>输入名称</th>
    <th>描述</th>
  </tr>
  <tr>
    <td><strong>弯曲</strong>灰度</td>
    <td>选择如何生成拼接路径：<br><ul><li><strong>UV 蒙版</strong>沿UV接缝生成路径。</li><li><strong>弯曲</strong>生成硬边缘附近的路径。</li><li><strong>自定义输入</strong>允许您控制使用映射生成路径的位置。<br>使用<strong>自定义输入</strong>时，将在高对比度区域生成路径。</li></ul></td>
  </tr>
  <tr>
    <td><strong>自定义输入</strong>灰度</td>
    <td>使用自定义纹理或锚点。</td>
  </tr>
</table>

## 参数

<table>
  <tr>
    <th>参数名称</th>
    <th>描述</th>
  </tr>
  <tr>
    <td><strong>蒙版模式</strong></td>
    <td>选择蒙版模式。<br><ul><li>UV 蒙版：基于UV 岛的蒙版。</li><li>弯曲：基于弯曲图的蒙版。</li><li>自定义输入：基于自定义输入纹理的蒙版。</li></ul></td>
  </tr>
  <tr>
    <td><strong>路径Smoothness</strong></td>
    <td>柔化应用缝合区域的路径。</td>
  </tr>
  <tr>
    <td><strong>路径位置</strong></td>
    <td>偏移路径位置。</td>
  </tr>
  <tr>
    <td><strong>拼合大小</strong></td>
    <td>调整缝合线的比例。</td>
  </tr>
  <tr>
    <td><strong>缝合宽度</strong></td>
    <td>调整线迹的宽度。</td>
  </tr>
  <tr>
    <td><strong>缝合长度</strong></td>
    <td>调整线迹的长度。</td>
  </tr>
  <tr>
    <td><strong>缝合圆度</strong></td>
    <td>调整线迹的圆度。</td>
  </tr>
  <tr>
    <td><strong>抖动</strong></td>
    <td>沿缝合线流动方向调整抖动。</td>
  </tr>
</table>

## 示例

<table>
  <tr>
    <td><img src="../../../assets/generators/examples/auto-stitcher/custom-input2.png" alt=""/></td>
    <td>此示例说明自定义输入如何创建拼接路径。 <br><ul><li>黑白base color显示了我们用作自动缝合器生成器的自定义输入的噪声纹理。</li><li>自动缝合器生成器正在遮盖红色图层，使红色缝合路径可见。</li><li>请注意，红色拼接路径会适合自定义输入纹理的足够大的黑白区域。 红色缝合绝不会从白色到黑色或从黑色到白色交叉。</li></ul><br>下图显示了用于创建此示例的简单图层设置。<br><br><img src="../../../assets/generators/examples/auto-stitcher/custom-input-layer-stack.png" alt=""/></td>
  </tr>
</table>
