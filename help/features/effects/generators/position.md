---
title: 位置
description: 了解如何使用Substance 3D Painter的位置生成器。
source-git-commit: b7770a9497f0db047433aec32c31b57f8dc13ae7
workflow-type: tm+mt
source-wordcount: '537'
ht-degree: 3%

---


# 位置

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../../assets/generators/icon_position.webp" alt=""/><br><strong>进入：</strong>网格，uv，距离</td>
    <td style="border: 0;" valign="top"><strong>描述</strong><br>位置生成器使用烘焙位置和世界空间正常映射，根据3D空间中的素材位置（如从上到下或从两侧到两侧）创建渐变蒙版。<br><br>位置生成器输出单色（黑白）纹理。 因此，它对于根据世界空间中的位置生成渐变蒙版非常有用。<br><br>图像输入需要绘制的位置和世界空间法线图。 <a href="../../../baking/baking.md">在此处了解有关烘焙的更多信息</a>。</td>
  </tr>
</table>

## 输入

| 输入名称 | 描述 |
| --- | --- |
| **纹理**&#x200B;颜色 | 使用自定义纹理或锚点。 |
| **位置渐变**&#x200B;颜色 | 使用烘焙的位置图。 |
| **世界空间法线**&#x200B;颜色 | 使用烘焙过的世界空间法线图。 |

## 参数

| 参数名称 | 描述 |
| --- | --- |
| **全局反转** | 合并所有效果后反转最终结果。 |
| **全局模糊** | 合并所有渐变后，统一模糊最终蒙版。 |
| **全局平衡** | 在所有渐变都位于黑色或白色之间后，调整最终蒙版的平衡，例如亮度调整。 |
| **全局对比度** | 合并所有渐变后，调整最终蒙版的对比度。 |
| **使用纹理** | 打开或关闭自定义纹理贴图的使用。 |

### 位置渐变

| 参数名称 | 描述 |
| --- | --- |
| **反转** | 仅反转位置渐变。 |
| **余额** | 仅调整位置渐变的平衡，将中点移向黑色或白色，就像亮度控制一样。 |
| **对比度** | 仅调整位置渐变的对比度/衰减。 |
| **亮度** | 仅调整位置渐变的明度。 |
| **从右到左** | 调整效果在网格上从左到右的应用方式。 |
| **从上到下** | 调整效果在网格上从上到下应用的方式。 |
| **从前到后** | 调整效果在网格上从前到后的应用方式。 |

#### 放置渐变/从右到左

| 参数名称 | 描述 |
| --- | --- |
| **反转** | 反转从右到左的渐变方向。 |
| **混合模式** | 选择要用于从右到左渐变的[混合模式](../../../interface/layer-stack/blending-modes.md)。 |

#### 定位渐变/由上至下

| 参数名称 | 描述 |
| --- | --- |
| **反转** | 反转从上到下的渐变方向。 |
| **混合模式** | 选择要用于从上到下渐变的[混合模式](../../../interface/layer-stack/blending-modes.md)。 |

#### 放置渐变/从前到后的位置

| 参数名称 | 描述 |
| --- | --- |
| **反转** | 反转“从前到后”渐变方向。 |
| **混合模式** | 选择要用于前后渐变的[混合模式](../../../interface/layer-stack/blending-modes.md)。 |

### 纹理

<table>
  <tr>
    <th>参数名称</th>
    <th>描述</th>
  </tr>
  <tr>
    <td><strong>纹理不透明度</strong></td>
    <td>调整自定义纹理的可见性。</td>
  </tr>
  <tr>
    <td><strong>反相</strong></td>
    <td>反转自定义纹理映射。</td>
  </tr>
  <tr>
    <td><strong>灰度转换</strong></td>
    <td>设置从全色转换为灰度图像的方法。 <a href="grayscale-conversion.md">灰度转换生成器包含有关每个方法工作方式的更多信息</a>。</td>
  </tr>
  <tr>
    <td><strong>混合模式</strong></td>
    <td>选择要使用的<a href="../../../interface/layer-stack/blending-modes.md">混合模式</a>。</td>
  </tr>
  <tr>
    <td><strong>比例</strong></td>
    <td>调整自定义纹理的大小。</td>
  </tr>
  <tr>
    <td><strong>对比度</strong></td>
    <td>调整自定义纹理的对比度/衰减。</td>
  </tr>
  <tr>
    <td><strong>Brightness</strong></td>
    <td>调整自定义纹理的明度。</td>
  </tr>
  <tr>
    <td><strong>三平面</strong></td>
    <td>启用“<strong>使用三平面</strong>”后，纹理从三个方向（X、Y、Z轴）投影，而不是仅依赖于UV。 <br><ul><li>如果未启用三平面，纹理将遵循UV布局。</li><li>启用三平面后，纹理从多个角度投影并混合。</li></ul></td>
  </tr>
  <tr>
    <td><strong>三平面对比度</strong></td>
    <td>使用三平面映射投影纹理时，调整纹理混合的平滑程度。 这可以调整每个方向的投影之间混合的柔和度。</td>
  </tr>
</table>
