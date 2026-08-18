---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/features/post-processing/depth-of-field.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中使用深度的场后处理创建逼真的相机焦点模糊效果。
helpx_creative_field: ""
helpx_description: Painter > Features > Post Processing > Depth of Field
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 景深
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 4%

---


# 景深

![](../../assets/dof-example.jpg)![](../../assets/dof.png)

字段&#x200B;**(DOF)的**&#x200B;深度没有直接参数。 如果启用，它将&#x200B;**覆盖**&#x200B;来自&#x200B;**Iray**&#x200B;的DOF。

要控制视窗中的自由度外观，可通过“相机”进行两项设置：

| *设置* | *描述* |
| --- | --- |
| **焦距** | 定义焦点所在的距离。  此点由场效应深度使用。 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/focus-distance-optim.gif"/></div> **注意：**&#x200B;可使用快捷键&#x200B;**CTRL +鼠标中键单击网格的点，从而自动设置焦距。** |
| **光圈** | 定义字段深度的宽度。 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/dof-aperture-optim.gif"/></div> **注意：**&#x200B;如果Iray正在控制此参数，则更改它将重新触发计算。 |
