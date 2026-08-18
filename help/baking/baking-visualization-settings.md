---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/baking/baking-visualization-settings.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中配置烘焙可视化设置以预览和调试网格图烘焙结果。
helpx_creative_field: ""
helpx_description: Painter > Baking > Baking visualization settings
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 烘焙可视化设置
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 6%

---


# 烘焙可视化设置

![](../assets/viewport-vizu.png)

烘焙可视化是处于烘焙模式时Painter视窗中的面板。 它允许您调整与视区中网格显示相关的设置。

## 常规设置

| 设置 | 描述 |
| --- | --- |
| **隐藏烘焙网格** | 如果启用，此图标将在视区中隐藏高多边形和笼形网格。 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../assets/hide-baking-meshes.png"/></div> |
| **仅显示选定的纹理集** | 如果启用，则视区中只会显示当前活动“纹理集”的保持格和高多边形网格。 |

### 高清晰度网格 (HP)

| 设置 | 描述 |
| --- | --- |
| <b>网格</b> | 如果启用，将在3D视图中显示高多边形网格。 禁用后，也会从内存中卸载高多边形网格，这有助于提高性能。 使用此设置旁边的颜色选项可控制视区中的网格曲面颜色。 |
| <b>匹配错误</b> | 如果启用，则以给定颜色显示笼形网格壳外部的高多边形网格的区域。 此设置有助于识别在烘焙过程中将遗漏的区域，这些区域可能会导致丢失详细信息/信息。 使用此设置旁边的颜色选项可控制视区中相交区域的颜色。 |

### 包裹

| 设置 | 描述 |
| --- | --- |
| <b>笼形表面</b> | 如果启用，则在3D视图中将显示保持架网格曲面。 保持架的表面由设置旁边的颜色按钮定义。 |
| <b>笼形表面不透明度</b> | 使网格或多或少透明，以管理底层网格中的细节可见性。 |
| <b>笼线框</b> | 如果启用，网笼网格的线框将在视区中可见。 可以使用此设置旁边的“线框”按钮调整颜色。 |
| <b>笼线框不透明度</b> | 使线框或多或少透明。 |

### UV 接缝

| 设置 | 描述 |
| --- | --- |
| <b>硬边缘上缺少接缝</b> | 如果启用，非UV接缝的网格曲面上的硬边将用设置旁边的按钮定义的颜色加亮显示。 加亮的边仅在保持架和低多边形网格上可见。 在2D和3D视图中都可以看到边。 此设置可帮助识别具有拆分顶点法线而没有UV展开接缝的边缘，这可能会导致以后出现烘焙问题。 |

### 项目网格

<table data-preserve-html="true">
<colgroup><col/><col/><col/></colgroup><tbody><tr><th scope="col">设置</th>
<th scope="col">辅助设置</th>
<th scope="col">描述</th>
</tr><tr><td><b>项目网格</b></td>
<td> </td>
<td><p>如果启用，则用于烘焙高多边形网格的低多边形网格将在视区中可见。 如果启用了<b>“隐藏烘焙网格”</b>，则此设置也将自动启用，以避免出现空视区。</p>
<p>使用此设置旁边的颜色选项可调整项目网格的颜色。</p>
</td>
</tr><tr><td rowspan="7"><b>中性材质</b></td>
<td><b>质量</b></td>
<td>控制低多边形网格曲面上的Specular反射品质。 使用较高的值将在反射中实现更好的保真度，但较高的值可能会影响性能。 较低的值会在正常映射的着色中引入接缝（注意：这只是一个显示问题）。</td>
</tr><tr><td><b>粗糙度</b></td>
<td>控制视区中低多边形网格材料的粗糙度。</td>
</tr><tr><td><b>金属</b></td>
<td>控制视区中低多边形网格材料的金属性。</td>
</tr><tr><td><b>AO 强度</b></td>
<td>控制烘焙的环境遮蔽对视区中低多边形网格着色的贡献程度。</td>
</tr><tr><td><b>弯曲法线</b></td>
<td>如果启用，请使用烘焙的弯曲法线来改善视区中的低多边形网格着色。</td>
</tr><tr><td><b>弯曲法线散射量</b></td>
<td>控制弯曲法线对漫射着色的影响程度。</td>
</tr><tr><td><b>弯曲法线镜面量</b></td>
<td>控制弯曲法线对着色的影响程度。</td>
</tr></tbody></table>
