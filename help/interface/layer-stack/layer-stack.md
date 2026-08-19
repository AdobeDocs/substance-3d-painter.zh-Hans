---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/interface/layer-stack.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中使用图层栈叠来组织和管理多个纹理绘画图层。
helpx_creative_field: ""
helpx_description: Painter > Interface > Layer stack
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 图层堆叠
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 5%

---


# 图层堆叠

![](../../assets/layer-stack.png)

使用&#x200B;**图层栈栈**&#x200B;可以操作纹理集的图层。 图层包含绘画和各种效果，可在场景中的3D对象上创建纹理。 您可以隐藏和取消隐藏图层，将它们放入文件夹中并更改其不透明度和混合模式。

有关其他信息，请参阅以下页面：

* [创建图层](creating-layers.md)
* [管理图层](managing-layers.md)
* [蒙版和效果](masking-and-effects.md)
* [混合模式](blending-modes.md)
* [图层实例化](layer-instancing.md)
* [几何蒙版](geometry-mask.md)

## 概述

图层栈叠以特定层次结构显示图层：底部的图层将首先在网格上绘制，顶部的图层将随后绘制。 因此，位于栈栈顶部的图层是最后一个项目，而位于最底部的图层是第一个项目。 同样的原则也适用于文件夹，但文件夹的内容优先。 这意味着文件夹的内容将在同级图层之前处理。

**常见特征：**

* 每个图层为&#x200B;**多通道**。
* 绘画工具将在所有通道&#x200B;**上绘画**，具体取决于材质设置（您当前正在图层栈栈中查看的通道没有影响）。
* 每个图层都有&#x200B;**混合模式**&#x200B;和每个通道&#x200B;**不透明度**（您可以通过左上角的下拉菜单在通道之间切换）。

**图层的类型：**

* **绘画图层** ：此类型的图层可以使用画笔和粒子进行绘画
* **填充图层** ：无法在此图层上绘画，可以将素材加载到其中来填充通道。 （例如，也可以通过操控变换来重复使用素材。）
* **文件夹** ：此类型的图层仅用于包含其他图层，主要用于组织图层栈栈

在每个图层上，您可以&#x200B;**添加蒙版**，以便仅将内容应用于当前纹理集通道的特定部分。\
您可以手动（使用画笔进行灰度）在蒙版上绘画，也可以使用滤镜和物质来获得更动态/程序化的结果。

## 视图模式

![](../../assets/switch-viewmode-optim.gif)

图层栈栈的左上下拉菜单控制图层栈栈的视图模式。 由于图层可以覆盖多个通道，因此不可能同时显示所有这些属性。 因此，可使用视图模式来定义当前显示上下文。 使用此下拉菜单时，可以指定应使用哪些通道在图层缩览图中显示，以及仅控制此通道的混合模式和不透明度。

此下拉菜单中的列表基于[纹理集设置](../texture-set/texture-set-settings.md)中可用的通道列表。

## 操作

![](../../assets/image2020-9-30-12-2-13.png)

图标的右上角列表是可以在图层栈栈中执行的常见操作：

| 操作 | 描述 |
| --- | --- |
| 添加效果 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/icon-effect.png"/></div> | 创建一个新效果并将其添加到当前选定的图层。 有关效果的更多信息，请参阅[专用页面](../../features/effects/effects.md)。 |
| 创建蒙版 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/icon-mask.png"/></div> | 打开包含下列项目的蒙版操作菜单：<ul data-preserve-html="true"><li data-preserve-html="true">添加白色蒙版</li><li data-preserve-html="true">添加黑色蒙版</li><li data-preserve-html="true">添加位图蒙版</li><li data-preserve-html="true">添加带颜色选择的蒙版</li><li data-preserve-html="true">添加带高度组合的蒙版</li></ul> |
| 创建新绘画图层 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r3-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/image2020-9-30-11-52-41.png"/></div> | 在当前选定的图层上方创建一个新的绘画图层。 |
| 创建新的填充图层 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r4-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/image2020-9-30-12-0-49.png"/></div> | 在当前所选图层上方创建新的[填充图层](../../painting/fill-projections/fill-projections.md)。 |
| 添加新的智能素材 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r5-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/icon-smartmat.png"/></div> | 在当前选定的图层上方插入新的智能素材。单击此按钮将打开一个迷你架，以浏览当前[资源](../../interface/assets/assets.md)中可用的智能素材列表。 |
| 添加新文件夹 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r6-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/image2020-9-30-12-1-13.png"/></div> | 在当前选定的图层上方创建一个新的空文件夹。 |
| 删除图层 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r7-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/icon-trash.png"/></div> | 删除当前选定的项目（图层、文件夹或效果）。 |
