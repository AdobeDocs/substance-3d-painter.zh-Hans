---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/workflow-issues/tools-issues/paint-tool-bleeds-on-other-uv-islands.html"
breadcrumb-title: ''
description: 了解如何修复Substance 3D Painter中绘图工具渗出UV 岛的问题，以保持清晰的纹理边界。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Workflow Issues > Tools Issues > Paint Tool bleeds on other UV islands
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 在其他UV 岛上绘画工具出血
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# 在其他UV 岛上绘画工具出血

[绘图工具](../../../features/effects/paint.md)的某些默认行为在某些特定情况下可能看起来与直觉相反。 Substance 3D Painter是一款主要用于3D空间的应用程序，也适用于绘画。 绘画画笔的默认设置为在绘画时尝试在UV之间保持无缝对接。 这就是为什么在与2D视图交互时，某些结果可能看起来出乎意料。

若要避免在2D视图中绘画时其他UV 岛渗出，只需更改刀具参数中的&#x200B;**对齐**&#x200B;设置：

| *对齐模式* | *预览* |
| --- | --- |
| **正切绕排** | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../../assets/paint-mode-tangent-optim.gif"/></div> |
| **UV** | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../../assets/paint-mode-uv.gif" width="450px"/></div> |
