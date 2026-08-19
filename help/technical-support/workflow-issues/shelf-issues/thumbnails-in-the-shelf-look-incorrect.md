---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/technical-support/workflow-issues/shelf-issues/thumbnails-in-the-shelf-look-incorrect.html"
breadcrumb-title: ''
description: 了解如何修复Substance 3D Painter托架中显示的缩略图不正确，以确保准确预览资源。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Workflow Issues > Shelf Issues > Thumbnails in the shelf look incorrect
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 架子中的缩览图看起来不正确
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---


# 架子中的缩览图看起来不正确

如果架子中的缩览图看起来与常规缩览图不同，可能是因为用于渲染预览的着色器。

| 损坏的缩略图 | 正常缩略图 |
| --- | --- |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../../assets/shelf-broken-preview.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../../assets/shelf-normal-preview.png" width="300px"/></div> |

## 1 — 打开主设置窗口

转到&#x200B;**编辑**&#x200B;并单击&#x200B;**设置** ：

![](../../../assets/pref-menu.png)

## 2 — 移除架子预览着色器

在&#x200B;**常规**&#x200B;视图中，向下滚动直到“预览选项”部分可见。\
单击“**材质预览着色器**”前面的&#x200B;**交叉**&#x200B;按钮以移除指定的当前着色器。

![](../../../assets/remove-preview-shader.png){width="450px"}

## 3 — 重新启动Substance 3D Painter

为了重新生成缩览图以便它们看起来正确，需要重新启动Substance 3D Painter。
