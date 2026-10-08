---
breadcrumb-title: ""
description: 在Substance 3D Painter中使用每个UV拼贴的填充匹配来匹配UV拼贴之间的纹理模式，从而实现无缝拼贴。
title: 填充（按UV 平铺匹配）
user-guide-description: ""
user-guide-title: ""
source-git-commit: 6b6d52207ca1d043aaa1b2b14145b6b49d4c1942
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 1%
---

# 填充（按UV 平铺匹配）

**填充（每个UV 平铺匹配）**&#x200B;是一个特殊的2D投影，对[UV 平铺](../../features/uv-tiles/uv-tiles.md)项目很有用。 它允许从序列中为每个UV 平铺分配一个UDIM纹理。

此投影没有任何专用设置，因为会为每个UV 平铺分配一个或多个图像。 由于没有设置，因此此模式也比较适合性能。

| 模式 | 描述 |
| --- | --- |
| **UV 投影** | 单个图像或序列中的第一个图像将应用于所有UV拼贴。 这还可以提供变形控制，请参阅[UV 投影](uv-projection.md)了解更多详细信息。 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/uv-3.jpg" width="700px"/></div> |
| **填充（每个UV 平铺匹配）** | 序列中的每个图像都被指定给专用UV 平铺。 没有变形控件。 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/fill-match.jpg" width="700px"/></div> |
