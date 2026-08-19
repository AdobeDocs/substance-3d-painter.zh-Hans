---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/painting/fill-projections/spherical-projection.html"
breadcrumb-title: ''
description: 使用Substance 3D Painter中的球面投影功能投影球体中的纹理，以便围绕对象环绕纹理。
helpx_creative_field: ""
helpx_description: Painter > Painting > Fill projections > Spherical projection
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spherical projection
user-guide-description: ''
user-guide-title: ''
source-git-commit: 7e24e45387178db5efa813e64e4b86ac2ae2e5aa
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 2%

---


# Spherical projection

![](../../assets/spherical-proj.jpg)

填充球面投影允许围绕对象投影图像和图案。 在圆形对象上投影或将纹理扭曲为圆形图案将很有用。

## 属性

| 设置 | 描述 |
| --- | --- |
| **筛选** | 控制如何过滤纹理或素材。 此设置可能会影响多次重复时纹理的外观。 如果高缩放值使用的滤镜与默认滤镜不同，可能会产生更好的外观效果。 当前可用设置：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>双线性`\|`HQ</strong>（默认）：高级双线性过滤，尝试在拼贴值较高时改进纹理的品质。</li><li data-preserve-html="true"><strong>双线性`\|`锐化</strong>：简单的双线性滤波，略微平滑纹理，但尝试保留细节。</li><li data-preserve-html="true"><strong>最接近</strong>：无过滤，如果双线性过滤产生模糊结果并破坏细微细节，则非常有用。 可以在纹理中引入锯齿。</li></ul> |
| **UV 展开** | 控制纹理在投影中的重复方式。 可能的值为：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>无</strong>：纹理不重复。 纹理之外的任何内容都是黑色/透明的。</li><li data-preserve-html="true"><strong>水平重复</strong>：纹理仅水平重复。</li><li data-preserve-html="true"><strong>垂直重复</strong>：纹理仅垂直重复。</li><li data-preserve-html="true"><strong>重复</strong>（默认）：纹理在两个轴上重复。</li></ul> <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/spherical-repeat.jpg" width="500px"/></div> |
| **形状裁剪** | 定义投影纹理在投影区域之外是否可见。 可能的值为：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>项目已裁剪为形状</strong>：投影限制在投影区域内。</li><li data-preserve-html="true"><strong>投影延伸到形状</strong>之外（默认）：投影延伸到投影区域之外。</li></ul> <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r3-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/spherical-shape-crop.jpg" width="500px"/></div> |

### UV转换

UV变换设置控制投影中的纹理。

| *设置* | *描述* |
| --- | --- |
| **缩放** | 定义纹理在投影内将重复的次数。 |
| **旋转** | 控制应用于投影的纹理的角度。 |
| **偏移** | 控制投影的纹理的原点。 默认值表示纹理位于投影的中间。 |

### 3D projection settings

3D投影设置控制投影在3D空间中的变换。

| 设置 | 描述 |
| --- | --- |
| **偏移** | 投影在3D空间中的原点位置。 单位基于整个场景的定界框。 0是这个盒子的中心。 |
| **旋转** | 在每个轴上旋转整个投影的角度（以度为单位）。 |
| **缩放** | 每个轴上整个投影的大小。 |

## 上下文工具栏

位于视区顶部的[上下文工具栏](../../interface/toolbars.md)提供了多种设置和工具，可用于控制操纵器和投影：

| 图标 | 名称 | 描述 |
| --- | --- | --- |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r1-column-c0_image" src="../../assets/icon-hide-manipulator.png" width="50px"/></div> | 显示/隐藏操纵器 | 如果启用，操作器将在视区中可见并可控制。 |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r2-column-c0_image" src="../../assets/icon-manipulator-settings.png" width="50px"/></div> | 操纵器设置 | 此菜单包含三个设置：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>操纵器大小</strong>：控制操纵器在视区中的大小。</li><li data-preserve-html="true"><strong>网格步骤</strong>：定义使用约束进行转换时步骤的大小。</li><li data-preserve-html="true"><strong>角度步长</strong>：定义带约束旋转时步长的角度。</li></ul> |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r3-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/icon-translate.png" width="50px"/></div> | 平移机械手 | 允许沿主轴(X、Y、Z)移动场景中的投影。 |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r4-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/icon-rotate.png" width="50px"/></div> | 旋转机械手 | 允许沿主轴(X、Y、Z)旋转场景中的投影。 |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r5-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/icon-scale.png" width="50px"/></div> | 缩放机械手 | 允许沿主轴(X、Y、Z)缩放场景中的投影。 |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r6-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/icon-surface.png" width="50px"/></div> | 表面机械手 | 允许通过将投影捕捉到3D模型曲面上来移动投影。  **注意：**&#x200B;此操纵器仅适用于“平面”和“变形”投影类型。 |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r7-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/icon-space.png" width="50px"/></div> | 机械手空间 | 定义要在哪个空间执行变换。 可能的值为：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>局部空间</strong>：轴与当前变换对齐。</li><li data-preserve-html="true"><strong>世界空间</strong>：轴与场景对齐。</li></ul> |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r8-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/icon-flip-x.png" width="50px"/></div> | X轴镜像 | 在X轴上翻转变换。 |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r9-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/icon-flip-y.png" width="50px"/></div> | Y轴镜像 | 在Y轴上翻转变换。 |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r10-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/icon-flip-z.png" width="50px"/></div> | Z轴镜像 | 在Z轴上翻转变换。 |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r11-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/icon-reset.png" width="50px"/></div> | 重置变换 | 将投影转换恢复为默认状态。 |

## 机械手

此投影操纵器仅在[3D视口](../../interface/viewport/3d-view.md)中可用。

| 操作 | 快捷键 | 描述 |
| --- | --- | --- |
| **翻译** | 鼠标单击 | 使用平移操作器，单击轴可移动投影：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>一个轴</strong>：仅向投影的一个方向移动。</li><li data-preserve-html="true"><strong>两个轴</strong>：在与轴对齐的计划上移动投影。</li><li data-preserve-html="true"><strong>三个轴</strong>：在相机空间中移动投影（计划对面）。</li></ul>   <table> <tr style="border: 0;"> <td style="border: 0;" valign="top">  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r1-column-c2_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/3d-translate.gif" width="200px"/></div>  </td> <td style="border: 0;" valign="top">  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r1-column-c2_dynamic_grid_items_grid-cell1_position-par_image" src="../../assets/3d-translate-2axes.gif" width="200px"/></div>  </td> <td style="border: 0;" valign="top">  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r1-column-c2_dynamic_grid_items_grid-cell2_position-par_image" src="../../assets/3d-translate-3axes.gif" width="200px"/></div>  </td> </tr> </table> |
| **转换受限** | 按住SHIFT键并单击鼠标 | 使用平移操纵器沿所选轴移动投影，但仅以特定间隔（步进）移动。 区间的大小通过机械手设置来定义。 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r2-column-c2_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/3d-translate-step.gif" width="200px"/></div> |
| **旋转** | 鼠标单击 | 使用“旋转”操纵器单击一个轴可旋转投影。 在轴之间单击允许同时旋转所有轴。   <table> <tr style="border: 0;"> <td style="border: 0;" valign="top">  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r3-column-c2_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/3d-rotate.gif" width="200px"/></div>  </td> <td style="border: 0;" valign="top">  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r3-column-c2_dynamic_grid_items_grid-cell1_position-par_image" src="../../assets/3d-rotate-3axes.gif" width="200px"/></div>  </td> </tr> </table> |
| **旋转受限** | 按住SHIFT键并单击鼠标 | 使用旋转机械手时，单击一个轴来旋转投影将仅在特定的间隔发生。 步长通过机械手设置由角度来定义。 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r4-column-c2_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/3d-rotate-step.gif" width="200px"/></div> |
| **缩放** | 鼠标单击 | 使用“缩放”操纵器单击一个轴手柄可沿给定轴调整投影的大小。   <table> <tr style="border: 0;"> <td style="border: 0;" valign="top">  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r5-column-c2_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/scale-one-axis.gif" width="200px"/></div>  </td> <td style="border: 0;" valign="top">  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r5-column-c2_dynamic_grid_items_grid-cell1_position-par_image" src="../../assets/scale-two-axis.gif" width="200px"/></div>  </td> <td style="border: 0;" valign="top">  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r5-column-c2_dynamic_grid_items_grid-cell2_position-par_image" src="../../assets/scale-3-axes.gif" width="200px"/></div>  </td> </tr> </table> |
| **缩放受限** | 按住SHIFT键并单击鼠标 | 使用“缩放”操纵器，在保持快捷键的同时单击一个轴手柄将逐步调整投影的大小。 步长大小与平移机械手相同。 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r6-column-c2_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/scale-1-axis-constrained.gif" width="200px"/></div> |
| **表面** | 鼠标单击 | 使用“曲面”操纵器时，单击并将其拖动到3D模型上会将其捕捉到曲面上。 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r7-column-c2_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/surface.gif" width="200px"/></div> **注意：**&#x200B;此机械臂仅适用于&#x200B;**平面**&#x200B;和&#x200B;**变形**&#x200B;投影类型。 |
