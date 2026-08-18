---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/interface/layer-stack/geometry-mask.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中使用几何蒙版来根据网格几何形状和表面属性遮盖图层。
helpx_creative_field: ""
helpx_description: Painter > Interface > Layer stack > Geometry mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 几何蒙版
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '736'
ht-degree: 1%

---


# 几何蒙版

![](../../assets/geometry-mask.png)\
几何图形蒙版是图层上的辅助蒙版，允许基于关联纹理集的3D模型几何图形来蒙版图层。 它可以按网格名称或UV磁贴进行蒙版。

## 概述

几何蒙版的工作方式是指定图层应通过包含/排除列表应用于3D模型的哪个部分。

几何蒙版是快速丢弃3D模型几何大片区域的有用工具。 它为绘画蒙版提供了几个优点：

* 设置视口选择模式并搭配使用通常会更快一些。
* 该算法在生成纹理时，可以完全丢弃几何信息，因此具有较好的性能。
* 它是非破坏性的，并且将在重新导入后3D模型更改时更新。
* 它可以在蒙版几何下方绘制几何，从而绘制隐藏部分。
* 与绘画蒙版一样，可以将几何图形蒙版应用于组以同时影响多个图层。

### 图标状态

几何蒙版图标可指示其状态：

| 图标 | 描述 |
| --- | --- |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/geo-mask-icon-default.png"/></div> | 未排除任何几何，图层将应用于关联纹理集的整个网格。这是任何新图层或文件夹的默认状态。 |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/geo-mask-icon-selection.png"/></div> | 已排除一个或多个网格名称。 编号指示图层仍然影响的剩余元素的数量。 |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r3-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/geo-mask-icon-uvtiles.png"/></div> | 已排除一个或多个UV磁贴。 编号指示图层仍然影响的剩余元素的数量。 |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r4-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/geo-mask-icon-empty.png"/></div> | 不包含网格名称，图层将没有任何实际效果。 |

## 编辑几何图形蒙版

要修改给定图层的几何图形蒙版，只需单击专用图标即可。 要退出编辑模式，只需单击图层的另一部分，如内容或绘画蒙版：

![](../../assets/geo-mask-editing.gif)

### 蒙版类型

几何蒙版支持两种类型的蒙版：

| 类型 | 描述 |
| --- | --- |
| **UV磁贴** | 通过指定应包含的UV磁贴(UDIM)编号来完成蒙版。 这是最有效的方法，它允许完全放弃计算纹理。 |
| **网格名称** | 蒙版是通过指定应包含在3D模型中的子网格来完成。 几何按网格名称分组。 |

### 图层栈栈操作

![](../../assets/geo-mask-actions.png)

通过右键单击图标，可以直接从图层栈叠中快速修改几何蒙版状态。

它提供以下操作：

| 操作 | 描述 |
| --- | --- |
| **复制几何蒙版** | 复制给定图层的几何图形蒙版的类型和选区。 |
| **粘贴到几何蒙版中。** | 粘贴之前复制的几何蒙版属性。 |
| **包含全部** | 将给定蒙版的所有元素标记为已选定。 |
| **排除全部** | 将给定蒙版的所有元素标记为取消选择。 |

## 通过蒙版几何图形绘画

排除几何的部分后，可在视区中隐藏。 这允许在先前不可访问的底层几何上进行绘制。

要隐藏排除的几何，请使用上下文工具栏中视区顶部的按钮：

![](../../assets/hide-excluded-geo-button.png)

在下面的示例中，3D模型已被拆分为两个对象：顶部和底部。 默认情况下，画笔描边与所有对象发生冲突。 通过排除顶部，现在可以仅涂抹底部。

>[!NOTE]
>
> 几何蒙版包含/排除列表是动态的，更改其状态将触发图层中画笔描边的新计算。 这样，在使用新的UV磁贴重新导入网格或网格名称已更改时，可以调整蒙版而不会丢失画笔描边。 但是，这也意味着画笔描边未经烘焙，因此几何蒙版中的任何更改都可能会导致之后的画笔投影不正确。

| 视觉 | 描述 |
| --- | --- |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r1-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/no-geo-excluded.jpg" width="420px"/></div> | 几何图形蒙版中未排除任何几何图形，白色画笔描边已在其上完成的绘画图层将与所有几何图形发生碰撞。禁用“**隐藏排除的几何图形**”按钮。 |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r2-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/geo-excluded-hidden.jpg" width="420px"/></div> | 顶部已在几何图形蒙版中排除，白色画笔描边仅与几何图形的底部冲突。已启用&#x200B;**隐藏排除的几何**&#x200B;按钮。 |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r3-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/geo-excluded-visible.jpg" width="420px"/></div> | 顶部已在几何图形蒙版中排除，白色画笔描边仅与几何图形的底部冲突。禁用“**隐藏排除的几何图形**”按钮。 |
