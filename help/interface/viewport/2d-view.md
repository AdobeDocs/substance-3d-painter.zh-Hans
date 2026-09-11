---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/interface/viewport/2d-view.html"
breadcrumb-title: ''
description: 了解如何使用Substance 3D Painter中的2D 视图查看和编辑UV空间中的纹理，以精准纹理绘画。
helpx_creative_field: ""
helpx_description: Painter > Interface > Viewport > 2D view
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 2D 视图
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 1%

---


# 2D 视图

![](../../assets/2d-view.jpg){width="450px"}

2D 视图显示当前所选[网格](../texture-set/texture-set.md)中的纹理集UV 岛。 它允许查看图层堆叠中的纹理，还允许在网格UV 岛上绘画。

## 显示模式

![](../../assets/display-mode-1.png)

视口右上角是显示模式下拉菜单。 此控件允许更改视口中应显示的信息。 它允许使用光照显示单通道、网格图或最终材料结果。

## 轴信息

![](../../assets/2d-axis.png)

视口右下角是&#x200B;**轴信息**，它指示二维轴的方向。 如果2D 视图是U和V，则说明轴

## UV 平铺信息

![](../../assets/2d-view-button.png)

**显示模式**&#x200B;旁边是&#x200B;**UV 平铺信息**&#x200B;按钮，用于显示/隐藏与UV 平铺相关的信息。 此按钮在常规项目中不可见。

## 项目工作流

根据创建项目时定义的工作流程，2D 视图的外观和行为可能会有所不同：

| *项目工作流* | *行为* |
| --- | --- |
| **常规项目** | 对于常规项目，只能绘制UV范围为[0-1]的UV。 此范围之外的任何内容都可见，但不会交互。在此示例中，只能绘制左侧的UV 岛（后面带有浅灰色背景）。 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/2d-view-range-regular.jpg" width="500px"/></div> |
| **UV 平铺项目** | 对于UV 平铺项目，每个UV范围都是一组可以绘制的新纹理。 此2D 视图将显示一个网格，以便更好地查看每个拼贴的整理方式。 每个磁贴都将分配一个UDIM号。 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/2d-view-range-uvtiles.jpg" width="500px"/></div> |
