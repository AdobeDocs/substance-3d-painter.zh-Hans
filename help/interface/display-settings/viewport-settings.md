---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/interface/display-settings/viewport-settings.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中配置视口设置以自定义显示选项和渲染品质。
helpx_creative_field: ""
helpx_description: Painter > Interface > Display settings > Viewport settings
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Viewport settings
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 1%

---


# Viewport settings

**显示设置**&#x200B;的此部分控制与视口显示相关的各种设置，例如纹理筛选和网格线框。

## Texture filtering

![](../../assets/texture-filtering.png)

各向异性筛选和镜像转换偏差允许控制视口中纹理的显示。 这些设置不会直接影响纹理，并且不会在导出时应用，它们只是优化视口中的渲染过程。 偏差设置允许对远离或倾斜的像素强制使用非常锐利的纹理，但在某些情况下，这些像素可能会创建莫尔图案或抖动。

默认设置是质量和性能的折中方案，应仅在真正需要时更改。

| *设置* | *描述* |
| --- | --- |
| **各向异性筛选** | 各向异性筛选改善了以斜角观看时的纹理质量。 高品质值可提供更好的筛选，但可能导致性能损失。 此设置可控制用于筛选的每像素的采样量(spp) ：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>已禁用</strong> ：无筛选</li><li data-preserve-html="true"><strong>低</strong> (2spp)</li><li data-preserve-html="true"><strong>中</strong> (4spp) ：默认值</li><li data-preserve-html="true"><strong>高</strong> (8spp)</li><li data-preserve-html="true"><strong>非常高</strong> (16spp)</li></ul> <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/quality-anisotropic-filtering.jpg"/></div> |
| **镜像转换偏差** | 偏移细节多级渐远纹理级别以提高纹理质量。 锐化值可能导致性能下降和锯齿状纹理。<ul data-preserve-html="true"><li data-preserve-html="true"><strong>0 — 柔和</strong> （轻量级性能） ：默认值</li><li data-preserve-html="true"><strong>1 — 中等柔和</strong></li><li data-preserve-html="true"><strong>2 — 清晰</strong></li><li data-preserve-html="true"><strong>3 — 非常锐利</strong> （性能密集）</li></ul>（从0到–3） |

## 帧

![](../../assets/camera-frame.png)

有关相机管理的详细信息，请参阅： [相机管理](../viewport/camera-management.md)

## 工具显示

![](../../assets/viewport-tool.png)

| *设置* | *描述* |
| --- | --- |
| **绘画时隐藏模板** | 使用模板时（请参阅绘画工具属性），此设置允许在网格上绘画时暂时隐藏该工具。 |
| **模板的显示不透明度** | 控制未绘画时模板在视口渲染上的可见性。 |
| **预览通道**&#x200B;投影 | 控制使用投影工具时显示的材料通道。 |

## Mesh wireframe

![](../../assets/viewport-mesh.png)

| *设置* | *描述* |
| --- | --- |
| **显示线框** | 启用或禁用视口中网格线框的显示。 |
| **线框** | 控制用于绘制线框的颜色。 |
| **线框不透明度** | 控制线框在网格顶部绘制时的可见程度。 |

## Channel display

![](../../assets/viewport-channel.png)

>[!NOTE]
>
> 仅在使用&#x200B;**单通道**&#x200B;查看模式时，声道显示设置才可用。

| *设置* | *描述* |
| --- | --- |
| **显示没有光照的独奏视图（无光）** | 在单通道模式下查看时，启用此设置将移除光照并将通道显示为平面色。 如果禁用，将在网格的边界应用阴影。 |
| **缩放HDR 值** | 在单通道模式下查看&#x200B;**HDR**&#x200B;纹理（如Height）时，此设置将缩放总值。 这对于查看超过1或低于–1的值非常有用。 结果等于&#x200B;**被比例驱动的通道**。在下面的示例中，Height声道的值最多为3。 但在默认情况下，除非更改比例值，否则无法查看比例值： <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r2-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/scale-hdr.jpg"/></div> |
| **将+/ — 颜色用于HDR值** | 此设置允许通过用第一种颜色替换正值和用第二种颜色替换负值来更轻松地查看纹理。 中性值(0)为黑色。示例： <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r3-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/colored-hdr.jpg"/></div> |
| **颜色通道** | 修改视口视图模式，以仅单独显示当前通道的R、G、B或Alpha分量。 此设置在“材质”显示模式下不可用。 启用后，所选颜色通道的名称会显示在视口中：  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r4-column-c1_image" src="../../assets/color-channel.png"/></div>  可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>RGBA</strong>（默认）：在颜色通道上，显示所有具有透明度的组件。</li><li data-preserve-html="true"><strong>灰度+Alpha</strong>（默认）：在灰度通道上，使用透明度显示灰度值。</li><li data-preserve-html="true"><strong>R</strong>：在颜色通道上，仅显示“红色”组件。</li><li data-preserve-html="true"><strong>G</strong>：在颜色通道上，仅显示绿色组件。</li><li data-preserve-html="true"><strong>B</strong>：在颜色通道上，仅显示蓝色组件。</li><li data-preserve-html="true"><strong>Alpha</strong>：在任何通道上，仅显示纹理的透明度。</li></ul> |

## 网格

![](../../assets/display-settings-grid.png)

使用网格设置可以显示和控制3D网格在3D视口内的绘制。

网格划分是根据当前相机的缩放比例和角度自动进行的。 当前网格单位显示在视区的左下角。

| 设置 | 描述 |
| --- | --- |
| **显示网格** | 如果启用，请使网格在3D视口中可见。 |
| **轴** | 定义网格在视口中可见的轴。 默认值为Y ，因为这是应用程序的启动轴。 |
| **网格颜色** | 在视口中绘制时网格的颜色。 |
| **网格不透明度** | 视口中网格的不透明度。 |
