---
title: Curvature
description: 了解如何使用Substance 3D Painter的弯曲生成器。
source-git-commit: b095b9b437f75bbb3a3b85ee84a6850026c3bf98
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 4%

---


# 弯曲

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../../assets/generators/icon_curvature.webp" alt=""/><br><strong>英寸：</strong>蒙版，生成器，灰度，混合</td>
    <td style="border: 0;" valign="top"><strong>描述</strong><br>弯曲生成器会根据烘焙的弯曲图创建蒙版，并可以选择将纹理或微细节混合到蒙版中。<br><br>弯曲生成器输出黑白纹理。 因此，在生成蒙版而不是直接应用于图层时非常有用。<br><br>需要烘焙的位置映射作为输入。 <a href="../../../baking/baking.md">在此处了解有关烘焙的更多信息</a>。</td>
  </tr>
</table>

## 输入

| 输入名称 | 描述 |
| --- | --- |
| **纹理**&#x200B;颜色 | 使用自定义纹理或锚点。 |
| **微正常**&#x200B;颜色 | 使用自定法线纹理或锚点。 |
| **微Height**&#x200B;颜色 | 使用自定义纹理或锚点。 |
| **弯曲**&#x200B;灰度 | 使用弯曲图。 |
| **世界空间法线**&#x200B;颜色 | 使用烘焙的世界空间法线映射。 |
| **位置渐变**&#x200B;颜色 | 使用烘焙的位置图。 |

## 参数

| 参数名称 | 描述 |
| --- | --- |
| **全局反转** | 合并所有效果后反转最终结果。 |
| **全局模糊** | 在合并所有效果后，统一柔化最终蒙版。 |
| **全局平衡** | 在黑色或白色之间组合所有效果后，改变最终蒙版的平衡，例如亮度调整。 |
| **全局对比度** | 在合并所有效果后调整最终蒙版的对比度。 |
| **使用纹理** | 打开或关闭自定义纹理映射的使用。 |
| **使用微详细信息** | 打开或关闭自定义微详细信息映射的使用情况。 |

### 弯曲

<table>
  <tr>
    <th>参数名称</th>
    <th>描述</th>
  </tr>
  <tr>
    <td><strong>反相</strong></td>
    <td>反转生成的弯曲图。</td>
  </tr>
  <tr>
    <td><strong>模式</strong></td>
    <td>设置弯曲模式。 <br><ul><li><strong>边缘</strong>：遮盖边缘（凸形区域）</li><li><strong>空腔</strong>：遮盖空腔（凹形区域）</li><li><strong>双</strong>：遮盖凹形和凸形区域。</li><li><strong>未处理</strong>：正常弯曲蒙版。</li></ul></td>
  </tr>
  <tr>
    <td><strong>锐化</strong></td>
    <td>调整锐化弯曲细节的强度。</td>
  </tr>
  <tr>
    <td><strong>精细</strong></td>
    <td>调整精细弯曲细节的强度。</td>
  </tr>
  <tr>
    <td><strong>柔和</strong></td>
    <td>调整柔和弯曲细节的强度。</td>
  </tr>
  <tr>
    <td><strong>中</strong></td>
    <td>调整中等弯曲细节的强度。</td>
  </tr>
  <tr>
    <td><strong>Large</strong></td>
    <td>调整大型弯曲细节的强度。</td>
  </tr>
  <tr>
    <td><strong>大</strong></td>
    <td>调整大弯曲细节的强度。</td>
  </tr>
  <tr>
    <td><strong>巨大</strong></td>
    <td>调整巨大弯曲细节的强度。</td>
  </tr>
  <tr>
    <td><strong>对比度</strong></td>
    <td>调整弯曲的对比度/衰减。</td>
  </tr>
  <tr>
    <td><strong>Brightness</strong></td>
    <td>调整弯曲的发光度。</td>
  </tr>
</table>

### 纹理

<table>
  <tr>
    <th>参数名称</th>
    <th>描述</th>
  </tr>
  <tr>
    <td><strong>纹理不透明度</strong></td>
    <td>控制自定义纹理的可见性。</td>
  </tr>
  <tr>
    <td><strong>反相</strong></td>
    <td>仅反转自定义纹理。</td>
  </tr>
  <tr>
    <td><strong>灰度转换</strong></td>
    <td>选择用于将彩色输入转换为黑白输入的方法。 </td>
  </tr>
  <tr>
    <td><strong>混合模式</strong></td>
    <td>为自定纹理设置混合模式。</td>
  </tr>
  <tr>
    <td><strong>比例</strong></td>
    <td>调整自定义纹理的大小。</td>
  </tr>
  <tr>
    <td><strong>对比度</strong></td>
    <td>设置自定义纹理的对比度/衰减。</td>
  </tr>
  <tr>
    <td><strong>Brightness</strong></td>
    <td>设置自定义纹理的明度。</td>
  </tr>
  <tr>
    <td><strong>三平面</strong></td>
    <td>启用“三平面”后，纹理从三个方向(X、Y、Z轴)投影，而不是仅依赖UV。 <br><ul><li>如果未启用三平面，纹理将遵循UV布局。</li><li>启用三平面后，纹理从多个角度投影并混合。</li></ul></td>
  </tr>
  <tr>
    <td><strong>三平面对比度</strong></td>
    <td>使用三平面映射调整纹理投影时的混合平滑度。 这将调整各个方向投影之间混合的柔和度。</td>
  </tr>
</table>

### 微细节

<table>
  <tr>
    <th>参数名称</th>
    <th>描述</th>
  </tr>
  <tr>
    <td><strong>微型Height</strong></td>
    <td>打开或关闭自定义微高度图的使用。</td>
  </tr>
  <tr>
    <td><strong>微法线</strong></td>
    <td>打开或关闭自定义微法线图的使用。</td>
  </tr>
  <tr>
    <td><strong>弯曲类型</strong></td>
    <td>设置弯曲类型。 <br><ul><li><strong>标准</strong>：生成的结果通常非常锐利，但可能缺少更宽的细节。</li><li><strong>Sobel</strong>：与标准结果类似，但稍微模糊一些，因为它使用Sobel滤镜评估法线图。</li><li><strong>平滑</strong>：生成不同级别的模糊（如mipmap）以累积信息。 这通常可提供更平滑的曲线，但可能会丢失细节。</li></ul></td>
  </tr>
  <tr>
    <td><strong>弯曲强度</strong></td>
    <td>在<strong>标准</strong>和<strong>Sobel </strong>弯曲模式下调整弯曲的强度。</td>
  </tr>
  <tr>
    <td><strong>Height细节强度</strong></td>
    <td>调整微Height细节的强度。</td>
  </tr>
</table>
