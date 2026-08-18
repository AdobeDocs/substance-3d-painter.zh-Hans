---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/painting/fill-projections/planar-projection.html"
breadcrumb-title: ''
description: 使用Substance 3D Painter中的平面投影功能从平面投影纹理，以便直接应用纹理。
helpx_creative_field: ""
helpx_description: Painter > Painting > Fill projections > Planar projection
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 平面投影
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '1165'
ht-degree: 2%

---


# 平面投影

![](../../assets/planar-proj-1.jpg)

填充的“平面”投影是3D投影，它将图像作为一个平面在一个方向上投影。 它可以用于在表面上或通过3D模型投射标志、贴花和其他图案。

## 属性

| *设置* | *描述* |
| --- | --- |
| **筛选** | 控制如何过滤纹理或素材。 此设置可能会影响多次重复时纹理的外观。 如果高缩放值使用的滤镜与默认滤镜不同，可能会产生更好的外观效果。 当前可用设置：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>两次线性 | HQ</strong>（默认）：高级双线性过滤，尝试在拼贴值较高时改进纹理的品质。</li><li data-preserve-html="true"><strong>两次线性 | Sharp</strong>：简单的双线性过滤，略微平滑纹理，但尝试保留细节。</li><li data-preserve-html="true"><strong>最接近</strong>：无过滤，如果双线性过滤产生模糊结果并破坏细微细节，则非常有用。 可以在纹理中引入锯齿。</li></ul> |
| **UV 展开** | 控制纹理在投影中的重复方式。 可能的值为：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>无</strong>：纹理不重复。 纹理之外的任何内容都是黑色/透明的。</li><li data-preserve-html="true"><strong>水平重复</strong>：纹理仅水平重复。</li><li data-preserve-html="true"><strong>垂直重复</strong>：纹理仅垂直重复。</li><li data-preserve-html="true"><strong>重复</strong>（默认）：纹理在两个轴上重复。</li></ul>  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c1_image" src="../../assets/planar-repeat.jpg" width="500px"/></div> |
| **形状裁剪** | 定义投影纹理在投影区域之外是否可见。 可能的值为：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>项目已裁剪为形状</strong>：投影限制在投影区域内。</li><li data-preserve-html="true"><strong>投影延伸到形状</strong>之外（默认）：投影延伸到投影区域之外。</li></ul>  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r3-column-c1_image" src="../../assets/shape-crop-toggle.gif" width="600px"/></div> |
| **深度剔除** | 如果启用，投影将沿其投影轴渐隐/切割，而不是无穷大。  <ul class="steps" data-preserve-html="true"> <li class="step" data-preserve-html="true">    <strong>已启用</strong>：<br/>       <img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r4-column-c1_procedure_proc_par_proc_step_step_par_image" src="../../assets/depth-culling-on.jpg" width="300px"/>   </li> <li class="step" data-preserve-html="true">    <strong>已禁用</strong>：<br/>       <img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r4-column-c1_procedure_proc_par_proc_step1_step_par_image" src="../../assets/depth-culling-off.jpg" width="300px"/> </li> </ul>  有一个参数可用：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>硬度</strong>设置控制深度剔除沿投影轴的硬度或柔和程度。</li></ul>  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r4-column-c1_image" src="../../assets/depth-culling-hardness.gif"/></div> |
| **背面剔除** | 如果启用，投影将不会显示在3D模型表面上远离投影轴的位置。有两个参数可用：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>角度</strong>：定义最小角度，该角度用于确定应忽略正在看见的面的时机。</li><li data-preserve-html="true"><strong>硬度</strong>：定义过渡的硬度或柔和程度。</li></ul>  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r5-column-c1_image" src="../../assets/backface-culling.gif"/></div> |

>[!NOTE]
>
> 通过调整变换比例，还可以控制投影深度：
> 
> ![](../../assets/planar-fade-optim.gif)

### UV转换

UV变换设置控制投影中的纹理/素材。

<table data-preserve-html="true" style="width: 100.0%;"><colgroup> <col style="width: 40.0%;"/> <col style="width: 20.0%;"/> <col style="width: 40.0%;"/> </colgroup><tbody><tr><th>缩放模式</th><th>设置</th><th>描述</th></tr><tr><td><p><strong>拼贴</strong>（默认）<strong> <br/></strong></p><p>允许手动设置当前纹理的重复量。</p></td><td><strong>平铺</strong></td><td>控制纹理的重复次数。</td></tr><tr><td rowspan="2"><br/><br/></td><td colspan="1"><strong>旋转</strong></td><td colspan="1">控制纹理投影到网格上的角度。</td></tr><tr><td colspan="1"><strong>位移</strong></td><td colspan="1">控制纹理的投影位置。 默认值表示纹理中心位于网格UV的中心。</td></tr><tr><th colspan="1"><br/></th><th colspan="1"><br/></th><th colspan="1"><br/></th></tr><tr><td rowspan="4"><p><strong>物理大小</strong></p><p>根据网格大小和嵌入的纹理自动调整物理尺寸。 它使用宽度和长度（X和Y度量）来计算正确的物理尺寸。 不考虑Z测量。</p><p>(有关详细信息，请参阅专用的[文档页面](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/features/physical-size))</p></td><td><strong>自定大小</strong></td><td><p>如果启用，则允许手动输入物理尺寸并覆盖资源提供的订阅。</p><p>如果未检测到物理尺寸，或者如果在同一图层/效果中使用了多个物理尺寸不同的资源，则会自动选择该选项。</p></td></tr><tr><td colspan="1"><strong>大小（厘米）</strong></td><td colspan="1">嵌入式物理尺寸以厘米为单位。 可以使用使用不同测量单位创建的网格文件 — 它将保持正确比例。 但是，资源大小当前仅以厘米显示。</td></tr><tr><td colspan="1"><strong>旋转</strong></td><td colspan="1">控制纹理投影到网格上的角度。</td></tr><tr><td colspan="1"><strong>位移</strong></td><td colspan="1"><p>控制纹理的投影位置。 默认值表示纹理中心位于网格UV的中心。</p></td></tr></tbody></table>

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
| **翻译** | 鼠标单击 | 使用平移操作器，单击轴可移动投影：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>一个轴</strong>：仅向投影的一个方向移动。</li><li data-preserve-html="true"><strong>两个轴</strong>：在与轴对齐的计划上移动投影。</li><li data-preserve-html="true"><strong>三个轴</strong>：在相机空间中移动投影（计划对面）。</li></ul>   <table> <tr style="border: 0;"> <td style="border: 0;" valign="top">  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r1-column-c2_dynamic_grid_items_image_794965934" src="../../assets/3d-translate.gif" width="200px"/></div>  </td> <td style="border: 0;" valign="top">  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r1-column-c2_dynamic_grid_items_image_1473363445" src="../../assets/3d-translate-2axes.gif" width="200px"/></div>  </td> <td style="border: 0;" valign="top">  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r1-column-c2_dynamic_grid_items_image" src="../../assets/3d-translate-3axes.gif" width="200px"/></div>  </td> </tr> </table> |
| **转换受限** | 按住SHIFT键并单击鼠标 | 使用平移操纵器沿所选轴移动投影，但仅以特定间隔（步进）移动。 区间的大小通过机械手设置来定义。  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r2-column-c2_image" src="../../assets/3d-translate-step.gif" width="200px"/></div> |
| **旋转** | 鼠标单击 | 使用“旋转”操纵器单击一个轴可旋转投影。 在轴之间单击允许同时旋转所有轴。   <table> <tr style="border: 0;"> <td style="border: 0;" valign="top">  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r3-column-c2_dynamic_grid_items_image" src="../../assets/3d-rotate.gif" width="200px"/></div>  </td> <td style="border: 0;" valign="top">  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r3-column-c2_dynamic_grid_items_image_1485982924" src="../../assets/3d-rotate-3axes.gif" width="200px"/></div>  </td> </tr> </table> |
| **旋转受限** | 按住SHIFT键并单击鼠标 | 使用旋转机械手时，单击一个轴来旋转投影将仅在特定的间隔发生。 步长通过机械手设置由角度来定义。  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r4-column-c2_image" src="../../assets/3d-rotate-step.gif" width="200px"/></div> |
| **缩放** | 鼠标单击 | 使用“缩放”操纵器单击一个轴手柄可沿给定轴调整投影的大小。   <table> <tr style="border: 0;"> <td style="border: 0;" valign="top">  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r5-column-c2_dynamic_grid_items_image" src="../../assets/scale-one-axis.gif" width="200px"/></div>  </td> <td style="border: 0;" valign="top">  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r5-column-c2_dynamic_grid_items_image_322064801" src="../../assets/scale-two-axis.gif" width="200px"/></div>  </td> <td style="border: 0;" valign="top">  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r5-column-c2_dynamic_grid_items_image_49230186" src="../../assets/scale-3-axes.gif" width="200px"/></div>  </td> </tr> </table> |
| **缩放受限** | 按住SHIFT键并单击鼠标 | 使用“缩放”操纵器，在保持快捷键的同时单击一个轴手柄将逐步调整投影的大小。 步长大小与平移机械手相同。  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r6-column-c2_image" src="../../assets/scale-1-axis-constrained.gif" width="200px"/></div> |
| **表面** | 鼠标单击 | 使用“曲面”操纵器时，单击并将其拖动到3D模型上会将其捕捉到曲面上。  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r7-column-c2_image" src="../../assets/surface.gif" width="200px"/></div>  **注意：**&#x200B;此机械臂仅适用于&#x200B;**平面**&#x200B;和&#x200B;**变形**&#x200B;投影类型。 |
