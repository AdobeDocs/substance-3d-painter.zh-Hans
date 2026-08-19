---
title: 灰度转换
description: 了解如何使用Substance 3D Painter的灰度转换生成器。
source-git-commit: b7770a9497f0db047433aec32c31b57f8dc13ae7
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 5%

---


# 灰度转换

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../../assets/generators/icon_grayscale_conversion.png" alt=""/><br><strong>英寸：</strong>生成器，灰度，颜色</td>
    <td style="border: 0;" valign="top"><strong>描述</strong><br>灰度转换生成器将纹理或地图转换为灰度值。<br><br>灰度转换生成器输出单色（黑白）纹理。 因此，它对于从全色输入映射生成蒙版非常有用。</td>
  </tr>
</table>

## 输入

| 输入名称 | 描述 |
| --- | --- |
| **源**&#x200B;颜色 | 使用自定颜色纹理或锚点。 |

## 参数

<table>
  <tr>
    <th>参数名称</th>
    <th>描述</th>
  </tr>
  <tr>
    <td><strong>灰度文字</strong></td>
    <td>设置灰度转换方法： <br><ul><li><strong>降低饱和度</strong>：使用RGB通道最强和最弱之间的中途值。</li><li><strong>亮度</strong>：使用与人眼感知亮度匹配的加权RGB系数（偏向绿色）。</li><li><strong>平均值</strong>：以相等量混合红色、绿色和蓝色通道。</li><li><strong>最大值</strong>：使用RGB通道中的最高值。</li><li><strong>最小值</strong>：使用RGB通道中的最小值。<ul><li>红色通道：仅使用红色通道。</li><li>绿色通道：仅使用绿色通道。</li><li>蓝色通道：仅使用蓝色通道。</li></ul></li></ul></td>
  </tr>
  <tr>
    <td><strong>反相</strong></td>
    <td>反转蒙版。</td>
  </tr>
  <tr>
    <td><strong>平衡</strong></td>
    <td>调整转换后的源图像的平衡，像亮度控制一样将中点向黑白方向移动。</td>
  </tr>
  <tr>
    <td><strong>对比度</strong></td>
    <td>定义转换后的源图像的对比度/衰减。</td>
  </tr>
  <tr>
    <td><strong>拼贴</strong></td>
    <td>设置转换后的源图像的拼贴。</td>
  </tr>
  <tr>
    <td><strong>旋转</strong></td>
    <td>调整转换后的源图像的角度。</td>
  </tr>
  <tr>
    <td><strong>安全旋转</strong></td>
    <td>打开或关闭安全旋转模式。 为true时，安全旋转将旋转锁定为45度角。</td>
  </tr>
</table>
