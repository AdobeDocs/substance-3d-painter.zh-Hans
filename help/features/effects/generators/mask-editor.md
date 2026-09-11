---
title: 蒙版编辑器
description: 了解如何使用Substance 3D Painter蒙版编辑器生成器。
source-git-commit: b7770a9497f0db047433aec32c31b57f8dc13ae7
workflow-type: tm+mt
source-wordcount: '1494'
ht-degree: 3%

---


# 蒙版编辑器

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../../assets/generators/icon_mask_editor_dark.png" alt=""/><strong>进入：</strong>蒙版，生成器</td>
    <td style="border: 0;" valign="top"><strong>描述</strong><br>蒙版编辑器生成器是一个多用途蒙版生成器，可让您将纹理、环境遮蔽、弯曲、世界空间法线、渐变、Thickness和微细节组合到单个蒙版中。<br>蒙版生成器生成器非常灵活，但由于其复杂性，与大多数生成器相比，它对性能的影响更大。<br><br>蒙版编辑器生成器输出单色（黑白）纹理。 因此，它对于基于各种已烘焙贴图生成蒙版非常有用。 <br><br>需要烘焙位置、Thickness、曲率、环境遮蔽和世界空间法线映射作为图像输入。 <a href="../../../baking/baking.md">在此处了解有关烘焙的更多信息</a>。</td>
  </tr>
</table>

## 输入

| 输入名称 | 描述 |
| --- | --- |
| **纹理**&#x200B;颜色 | 使用自定义纹理或锚点。 |
| **纹理（辅助）**&#x200B;颜色 | 使用自定义纹理或锚点。 |
| **世界空间法线**&#x200B;颜色 | 使用烘焙的世界空间法线映射。 |
| **位置渐变**&#x200B;颜色 | 使用烘焙的位置图。 |
| **Thickness**&#x200B;灰度 | 使用厚度图。 |
| **弯曲**&#x200B;灰度 | 使用弯曲图。 |
| **Ambient occlusion**&#x200B;灰度 | 使用烘焙的Ambient occlusion映射。 |
| **微正常**&#x200B;颜色 | 使用自定法线纹理或锚点。 |
| **微Height**&#x200B;颜色 | 使用自定义纹理或锚点。 |

## 参数

| 参数名称 | 描述 |
| --- | --- |
| **全局反转** | 合并所有图层后反转最终结果。 |
| **全局模糊** | 合并所有图层后，统一模糊最终蒙版。 |
| **全局平衡** | 在所有图层都在黑色或白色之间组合后，调整最终蒙版的平衡，例如亮度调整。 |
| **全局对比度** | 合并所有图层后，调整最终蒙版的对比度。 |
| **纹理不透明度** | 调整自定义纹理的可见性。 |
| **纹理2不透明度** | 调整第二个自定义纹理的可见性。 |
| **Ambient occlusion不透明度** | 调整ambient occlusion详细信息的可见性。 |
| **弯曲不透明度** | 调整弯曲详细信息的可见性。 |
| **世界空间法线不透明度** | 调整世界空间法线详细信息的可见性。 |
| **位置渐变不透明度** | 调整位置详细信息的可见性。 |
| **Thickness不透明度** | 调整Thickness详细信息的可见性。 |

### 纹理

<table>
  <tr>
    <th>参数名称</th>
    <th>描述</th>
  </tr>
  <tr>
    <td><strong>反相</strong></td>
    <td>反转自定纹理。</td>
  </tr>
  <tr>
    <td><strong>灰度转换</strong></td>
    <td>设置从全色转换为灰度图像的方法。 <a href="grayscale-conversion.md">灰度转换生成器包含有关每个方法工作方式的更多信息</a>。</td>
  </tr>
  <tr>
    <td><strong>混合模式</strong></td>
    <td>选择用于当前图层的<a href="../../../interface/layer-stack/blending-modes.md">混合模式</a>。</td>
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
    <td>启用<strong>“使用三平面”</strong>后，纹理将从三个方向(X、Y、Z轴)投影，而不是仅依赖UV。 <br><ul><li>如果未启用三平面，纹理将遵循UV布局。</li><li>启用三平面后，纹理从多个角度投影并混合。</li></ul></td>
  </tr>
  <tr>
    <td><strong>三平面对比度</strong></td>
    <td>使用三平面映射调整纹理投影时的混合平滑度。 这将调整各个方向投影之间混合的柔和度。</td>
  </tr>
  <tr>
    <td><strong>非方形拼贴</strong></td>
    <td>打开或关闭非方形拼贴。</td>
  </tr>
</table>

### 纹理2

<table>
  <tr>
    <th>参数名称</th>
    <th>描述</th>
  </tr>
  <tr>
    <td><strong>反相</strong></td>
    <td>反转自定义次要纹理。</td>
  </tr>
  <tr>
    <td><strong>灰度转换</strong></td>
    <td>设置从全色转换为灰度图像的方法。 <a href="grayscale-conversion.md">灰度转换生成器包含有关每个方法工作方式的更多信息</a>。</td>
  </tr>
  <tr>
    <td><strong>混合模式</strong></td>
    <td>选择用于当前图层的<a href="../../../interface/layer-stack/blending-modes.md">混合模式</a>。</td>
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
    <td>启用<strong>“使用三平面”</strong>后，纹理将从三个方向(X、Y、Z轴)投影，而不是仅依赖UV。 <br><ul><li>如果未启用三平面，纹理将遵循UV布局。</li><li>启用三平面后，纹理从多个角度投影并混合。</li></ul></td>
  </tr>
  <tr>
    <td><strong>三平面对比度</strong></td>
    <td>使用三平面映射调整纹理投影时的混合平滑度。 这将调整各个方向投影之间混合的柔和度。</td>
  </tr>
  <tr>
    <td><strong>非方形拼贴</strong></td>
    <td>打开或关闭非方形拼贴。</td>
  </tr>
</table>

### 环境光遮蔽

| 参数名称 | 描述 |
| --- | --- |
| **反转** | 反转“Ambient occlusion”和“微细节”图层。 |
| **混合模式** | 选择用于当前图层的[混合模式](../../../interface/layer-stack/blending-modes.md)。 |
| **模糊** | 调整Ambient occlusion和微细节柔和度。 |
| **余额** | 调整Ambient occlusion和微细节的平衡，像亮度控制一样将中点向黑白方向移动。 |
| **对比度** | 调整Ambient occlusion和微细节的对比度/衰减。 |

### 弯曲

<table>
  <tr>
    <th>参数名称</th>
    <th>描述</th>
  </tr>
  <tr>
    <td><strong>反相</strong></td>
    <td>反转弯曲。</td>
  </tr>
  <tr>
    <td><strong>混合模式</strong></td>
    <td>选择用于当前图层的<a href="../../../interface/layer-stack/blending-modes.md">混合模式</a>。</td>
  </tr>
  <tr>
    <td><strong>模式</strong></td>
    <td>设置弯曲模式。 <br><ul><li><strong>边缘</strong>：遮盖边缘（凸形区域）</li><li><strong>空腔</strong>：遮盖空腔（凹形区域）</li><li><strong>双</strong>：遮盖凹形和凸形区域。</li><li><strong>未处理</strong>：正常弯曲蒙版。</li></ul></td>
  </tr>
  <tr>
    <td><strong>锐化</strong></td>
    <td>调整锐化弯曲细节的可见性。</td>
  </tr>
  <tr>
    <td><strong>精细</strong></td>
    <td>调整精细弯曲细节的可见性。</td>
  </tr>
  <tr>
    <td><strong>柔和</strong></td>
    <td>调整软弯曲细节的可见性。</td>
  </tr>
  <tr>
    <td><strong>中</strong></td>
    <td>调整中等曲率细节的可见性。</td>
  </tr>
  <tr>
    <td><strong>Large</strong></td>
    <td>调整大型弯曲细节的可见性。</td>
  </tr>
  <tr>
    <td><strong>大</strong></td>
    <td>调整大曲率细节的可见性。</td>
  </tr>
  <tr>
    <td><strong>巨大</strong></td>
    <td>调整巨大弯曲细节的可见性。</td>
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

### 世界空间法线

| 参数名称 | 描述 |
| --- | --- |
| **反转** | 反转世界空间法线。 |
| **混合模式** | 选择用于当前图层的[混合模式](../../../interface/layer-stack/blending-modes.md)。 |
| **模糊** | 调整世界空间法线柔和度。 |
| **余额** | 调整世界空间法线的平衡，像亮度控制一样将中点向黑白方向移动。 |
| **对比度** | 调整世界空间法线的对比度/衰减。 |
| **亮度** | 调整世界空间法线的发光度。 |
| **从右到左** | 调整效果在网格上从左到右的应用方式。 |
| **从上到下** | 调整在网格中从上到下应用效果的方式。 |
| **从前到后** | 调整在网格中从前到后应用效果的方式。 |

### 世界空间法线/从右到左

| 参数名称 | 描述 |
| --- | --- |
| **反转** | 反转从右到左的方向。 |
| **混合模式** | 选择用于当前图层的[混合模式](../../../interface/layer-stack/blending-modes.md)。 |

### 世界空间法线/从上到下

| 参数名称 | 描述 |
| --- | --- |
| **反转** | 反转从上至下的方向。 |
| **混合模式** | 选择用于当前图层的[混合模式](../../../interface/layer-stack/blending-modes.md)。 |

### 世界空间法线/从前到后

| 参数名称 | 描述 |
| --- | --- |
| **反转** | 反转“从前到后”的方向。 |
| **混合模式** | 选择用于当前图层的[混合模式](../../../interface/layer-stack/blending-modes.md)。 |

### 位置渐变

| 参数名称 | 描述 |
| --- | --- |
| **反转** | 反转位置渐变图层。 |
| **余额** | 调整位置渐变图层的平衡，将中点向黑白方向移动，就像亮度控制一样。 |
| **对比度** | 调整位置渐变图层的对比度/衰减。 |
| **亮度** | 调整位置渐变图层的明度。 |
| **混合模式** | 选择用于当前图层的[混合模式](../../../interface/layer-stack/blending-modes.md)。 |
| **从右到左** | 调整效果在网格上从左到右的应用方式。 |
| **从上到下** | 调整在网格中从上到下应用效果的方式。 |
| **从前到后** | 调整在网格中从前到后应用效果的方式。 |

>[!TIP]
>
> 位置渐变由三个渐变组成，从右到左、从上到下以及从前到后。 每个子渐变都有其自己的混合模式，可用于创建不同的效果或遮蔽模型的不同区域。 这些渐变的混合模式仅彼此交互创建最终的位置渐变图层，而不会直接与生成器中位置渐变以外的其他图层交互。

### 位置渐变 — 从右到左

| 参数名称 | 描述 |
| --- | --- |
| **反转** | 反转从右到左的渐变方向。 |
| **混合模式** | 选择要用于从右到左渐变的[混合模式](../../../interface/layer-stack/blending-modes.md)。 |

### 位置渐变 — 从上到下

| 参数名称 | 描述 |
| --- | --- |
| **反转** | 反转从上到下的渐变方向。 |
| **混合模式** | 选择要用于从上到下渐变的[混合模式](../../../interface/layer-stack/blending-modes.md)。 |

### 位置渐变 — 从前到后

| 参数名称 | 描述 |
| --- | --- |
| **反转** | 反转“从前到后”渐变方向。 |
| **混合模式** | 选择要用于前后渐变的[混合模式](../../../interface/layer-stack/blending-modes.md)。 |

### 厚度

| 参数名称 | 描述 |
| --- | --- |
| **反转** | 反转Thickness。 |
| **模糊** | 调整Thickness图层中细节的柔和度。 |
| **对比度** | 调整Thickness图层的对比度/衰减。 |
| **亮度** | 调整Thickness图层的明度。 |

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
  <tr>
    <td><strong>AO半径</strong></td>
    <td>在微观细节中调整Ambient occlusion的半径（范围）。</td>
  </tr>
  <tr>
    <td><strong>AO深度</strong></td>
    <td>在微观细节中调整Ambient occlusion的深度（强度）。</td>
  </tr>
</table>
