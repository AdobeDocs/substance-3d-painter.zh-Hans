---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/interface/viewport/2d-view.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中使用2D视图查看和编辑UV空间中的纹理，以精确绘制纹理。
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

2D视图显示当前所选[UV 岛集](../texture-set/texture-set.md)中的网格纹理。 它不仅可以显示图层栈栈中的纹理，还可以在网格UV 岛上绘画。

## 显示模式

![](../../assets/display-mode-1.png)

视区的右上角是显示模式下拉菜单。 此控件允许更改在视区中应显示的信息。 它允许显示单个通道、网格图或带光照的最终素材结果。

## 轴信息

![](../../assets/2d-axis.png)

视区的右下角是&#x200B;**轴信息**，它指示二维轴的方向。 如果2D视图是U和V。

## UV拼贴信息

![](../../assets/2d-view-button.png)

**显示模式**&#x200B;旁边是&#x200B;**UV磁贴信息**&#x200B;按钮，用于显示/隐藏与UV磁贴相关的信息。 此按钮在常规项目中不可见。

## 项目工作流

根据创建项目时定义的工作流程，2D视图的外观和行为可能会有所不同：

| *项目工作流* | *行为* |
| --- | --- |
| **常规项目** | 使用常规项目时，只能绘制使用UV范围[0-1]的UV。 此范围之外的任何内容都可见，但不会交互。在此示例中，只能绘制左侧的UV 岛（后面带有浅灰色背景）。 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/2d-view-range-regular.jpg" width="500px"/></div> |
| **UV磁贴项目** | 利用UV拼贴项目，每个UV范围都是一组可以绘制的新纹理。 2D视图会显示网格，以更好地查看每个拼贴是如何组织的。 每个磁贴都将分配有一个UDIM编号。 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/2d-view-range-uvtiles.jpg" width="500px"/></div> |
