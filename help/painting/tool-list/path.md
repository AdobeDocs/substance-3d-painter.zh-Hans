---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/painting/tool-list/path.html"
breadcrumb-title: ''
description: 使用Substance 3D Painter中的路径工具创建和编辑路径，以实现精确的纹理绘画和描边放置。
helpx_creative_field: ""
helpx_description: Painting > Path tools list > Path tool
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 路径工具概述
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '1699'
ht-degree: 0%

---


# 路径工具概述

![显示鞋子上使用的路径工具的图像](../../assets/v90_banner_path.jpg)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>音频</b>

调整或添加音频到项目。


* 如果源视频有音频，请调整其音量。
* 添加、删除或替换外部音频文件。
* 调整外部音频文件音量。

</td>
<td style="border: 0;" valign="top">

![](../../assets/image_180.png)

</td>
</tr>
</table>

<b>路径工具</b>允许您定义具有网格曲面上的点的曲线。 创建曲线后，不同的“路径”工具允许您沿着曲线创建不同的效果。

## 创建路径

可以在绘画图层和绘画效果上创建路径。 有两种方法可访问路径工具：

* <b>通过界面</b>：导航到左侧的工具工具栏，然后单击顶部的第三个图标。
* <b>通过键盘快捷键</b>：默认情况下，未为该工具分配任何快捷键。 可通过编辑“选择沿路径绘画工具”快捷键，在“设置”菜单中对此进行更改。

选择该工具后，可通过单击3D视口内的3D模型曲面来放置点。 创建路径至少需要两个点（或顶点）。

![显示路径工具的选择以及点的创建的Gif](../../assets/path_create_points.gif)

路径工具具有不同的模式，它们可能与应用程序中提供的其他绘画工具类似：

* 沿路径绘制：沿定义的路径绘制常规画笔描边。
* [功能区路径](ribbon-tool.md)：沿路径绘制重复或拉伸的图像。
* [填充路径](filled-path.md)：使用统一的颜色填充路径的内部。
* 沿路径擦除：绘制沿定义路径擦除/删除信息的描边。
* 沿路径涂抹：绘制沿定义路径涂抹/模糊信息的描边。

![显示不同路径工具模式的工具工具栏的屏幕截图](../../assets/PathTools.png)

例如，<b>涂抹</b>模式下的路径工具会影响其他绘画信息：

![在涂抹模式下显示路径工具的Gif](../../assets/v90_path_smudge.gif)

>[!NOTE]
>
> <b>路径工具</b>仅在几何图形表面的3D空间中工作。 当前不支持在UV空间中或作为屏幕空间投影创建路径。

### 编辑路径

路径点（或顶点）自动附着在网格的曲面上。 它们可以随时移动和调整。 通过单击直线上的任意位置，可以向现有路径添加新顶点。 

* 按<b>Escape </b>或<b>Enter </b>将退出路径编辑。
* 退出后，单击网格的空白曲面将开始新路径。
* 将鼠标悬停并单击现有路径即可将其选中，从而允许继续或编辑该路径。 也可以通过<b>路径</b>面板重新选择路径（请参阅下文）。

![显示路径上新点添加和现有点移动的Gif](../../assets/path_edit_move_points.gif)

某些属性是特定于作为一个整体的路径。 在<b>属性</b>窗口中找到的选项就是这种情况。 就像使用常规描边一样（请参阅[绘画工具文档](paint-brush.md)），可以定义路径的以下属性：

* <b>画笔</b>
* <b>Alpha</b>
* <b>材质</b>

<b>画笔</b>部分包含仅适用于“路径”工具的其他选项：

| <b>设置</b> | <b>描述</b> |
| --- | --- |
| <b>投影深度</b> | 确定路径需要与网格曲面接近的程度，画笔图章才会显示。 要直接在视口中查看此视觉反馈，可以在<b>路径显示设置</b>中启用<b>法线</b>（请参阅下文）。 |
| <b>向上轴</b> | <b>跟随路径</b>关闭时用于定向画笔图章的轴。   在有些情况下，让所有图章沿全局轴/方向而不是沿路径对齐会更明智。 例如，在金属表面上使用铆钉。 |

其他属性是按路径上的点（顶点）定义的，例如压力。 要编辑特定点，只需单击它（或使用矩形选区）。 然后使用上下文工具栏编辑选定的点值。

![显示每个顶点的压力版本的Gif](../../assets/path_point_pressure_example.gif)

### 控制切线

有时，平滑路径并不理想，可能是因为它不遵循3D模型的最佳表面，也可能是因为它不适合特定的外观。 为了解决这些问题，可以修改给定顶点的切线。 切线是控制路径折弯方式的点的方向。

要在平滑或线性/断开切线之间切换，只需双击顶点（或使用上下文工具栏中的专用按钮）：

![显示如何控制路径上的切线的Gid](../../assets/path_break_tangents.gif)

要更精确地控制切线的方向，请使用上下文工具栏中的“自定切线”按钮手动覆盖它们：

![显示如何控制路径上的切线的Gid](../../assets/path_control_tangents.gif)

如果点尚未移动，请使用<b>ALT</b>键盘快捷键在移动时断开切线。

使用<b>CTRL</b>键盘快捷键可同时缩放两个切线。

>[!NOTE]
>
> 切线控件沿与路径中给定点的法向对齐的计划定义。 这意味着切线在某些方向上不能弯曲。

### 上下文工具栏

![路径模式下上下文工具栏的屏幕截图](../../assets/path_contextual_toolbar_overview.png)

选择<b>路径</b>工具时的<b>上下文工具栏</b>提供多种设置，可让您控制当前选定的路径：

| <b>参数</b> | <b>描述</b> |
| --- | --- |
| <b>显示/隐藏视口接口</b>  <div><img alt="路径工具显示隐藏图标" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_table_row-1k12728-column-xc227lz_image" src="../../assets/path_contextual_toolbar_showhide.png"/></div> | 如果启用，路径和顶点叠加将在视区中可见。 |
| <b>显示设置</b>  <div><img alt="“路径显示设置”图标" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_table_row-uj427cc-column-xc227lz_image" src="../../assets/path_contextual_toolbar_display.png"/></div> | 控制视区中路径可视反馈的外观：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>手柄大小</b>：控制路径点的尺寸。</li> <li data-preserve-html="true"><b>路径宽度</b>：控制路径线的Thickness。<br/> </li> <li data-preserve-html="true"><b>路径颜色</b>：控制路径线的颜色。<br/> </li> <li data-preserve-html="true"><b>未选择的路径颜色</b>：控制非活动路径的颜色。<br/> </li> <li data-preserve-html="true"><b>法线</b>：如果启用，则显示路径每个点上的投影方向。<br/> </li> <li data-preserve-html="true"><b>切线</b>：如果启用，则显示路径控制点的曲线方向。<br/> </li> <li data-preserve-html="true"><b>路径方向</b>：如果启用，则在路径末尾显示一个小箭头，以指示其绘画方向。 这对于了解描边中的图章的定向非常有用。</li> </ul>  <div><img alt="路径显示设置面板的屏幕截图" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_table_row-uj427cc-column-vo327hy_image" src="../../assets/path_contextual_toolbar_display_settings.png"/></div> |
| <b>反向路径方向</b>  <div><img alt="“反向路径方向”图标" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_table_row-5xb27rp-column-xc227lz_image" src="../../assets/path_contextual_toolbar_direction.png"/></div> | 翻转当前路径的方向。 方向定义了用于在描边内绘制图章的常规方向。 反转路径有助于重新定向绘制的图案。 |
| <b>切换转角/平滑</b>  <div><img alt="切换平滑角图标" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_table_row-8wd27al-column-xc227lz_image" src="../../assets/path_contextual_toolbar_smoothcorner.png"/></div> | 断开或对齐当前选定顶点的切线，以便在平滑曲线或线性曲线之间切换。  <div><img alt="同时具有平滑路径和线性路径的屏幕快照 " class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_table_row-8wd27al-column-vo327hy_image" src="../../assets/path_smooth_corner_demo.png"/></div>  **注意：**&#x200B;通过双击路径上的直接点，还可以在边角/平滑行为之间切换。 |
| <b>自定切线</b>  <div><img alt="自定切线的路径工具图标" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_table_row-r302zw8-column-xc227lz_image" src="../../assets/path_icon_custom_tangents.png"/></div> | 如果启用，则允许手动控制路径上给定点的切线。  <div><img alt="显示自定路径切线的图像" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_table_row-r302zw8-column-vo327hy_image" src="../../assets/paht_cutom_tangents_demo.png"/></div> |
| <b>开放/闭合路径</b>  <div><img alt="开放闭合路径图标" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_table_row-7ve27oq-column-xc227lz_image" src="../../assets/path_contextual_toolbar_close.png"/></div> | 打开或关闭当前路径。 要闭合路径，需要首先选择当前路径的两个端点之一。  <div><img alt="显示路径打开然后闭合的Gif" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_table_row-7ve27oq-column-vo327hy_image" src="../../assets/v90_path_open_close.gif"/></div> |
| <b>删除顶点</b>  <div><img alt="删除路径顶点的图标" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_table_row-v0f273z-column-xc227lz_image" src="../../assets/path_contextual_toolbar_delete.png"/></div> | 删除路径上当前选定的顶点。 |
| <b>对称</b>  <div><img alt="对称特征图标" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_table_row-hkg27qa-column-xc227lz_image" src="../../assets/path_contextual_toolbar_symmetry.png"/></div> | 启用或禁用当前路径的对称性。 有关详细信息，请参阅[对称文档](../symmetry/symmetry.md)。  <div><img alt="显示以对称方式绘制路径的Gif" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_table_row-hkg27qa-column-vo327hy_image" src="../../assets/v90_path_symmetry.gif"/></div> |
| <b>隐藏/忽略排除的几何</b>  <div><img alt="几何蒙版排除功能的图标" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_table_row-52h27be-column-xc227lz_image" src="../../assets/path_contextual_toolbar_exclude.png"/></div> | 如果启用，请通过隐藏的几何形状绘制当前路径。 有关详细信息，请参阅[几何蒙版文档](../../interface/layer-stack/geometry-mask.md)。 |

### “路径”面板

![路径面板](../../assets/path_panel_visibility.png)

>[!NOTE]
>
> 如果当前工具不是路径工具或者选择了填充图层/文件夹，则会隐藏面板。

视区内部是<b>路径</b>面板，其中列出了当前选定的绘画图层/效果的所有路径。 它提供了一种选择和管理路径的简单方法。

使用此面板，可以：

* 双击路径以<b>重命名</b>它。
* 通过选择路径，然后按Delete键，<b>删除</b>。
* <b>复制</b>/<b>粘贴</b>/<b>复制</b>具有专用键盘快捷键的路径。
* 使用眼睛图标<b>显示</b>或<b>隐藏</b>路径（控制路径是否应用于纹理化）。

为方便起见，还可以右键单击路径以打开提供相同操作的上下文菜单：

![路径面板右键单击菜单](../../assets/path_panel_rightclick_menu_copy_properties.png)

右键单击菜单还可打开操作以将路径的属性或位置复制到另一路径上。 这样可以轻松在不同路径之间共享或同步功能：

![显示如何复制和粘贴路径属性的Gif](../../assets/path_copy_paste_properties.gif)

![显示如何复制和粘贴路径位置的Gif](../../assets/path_copy_paste_vertices.gif)

>[!NOTE]
>
> 仅当路径基于相同的绘画工具时，复制和粘贴属性才有效。 例如，不能使用涂抹设置在一个路径和使用画笔设置的另一个路径之间共享属性。

## 工具预设

![选择路径工具时，“属性”面板“预设”部分的屏幕截图](../../assets/path_presets.png){width="400px"}

选择路径工具后，“属性”面板顶部将显示预设部分。 在这里，您可以快速访问各种路径工具的预设。

### 收藏路径预设

预设部分中的收藏夹选项仅包含您收藏的预设，可让您更快地访问这些预设。 要开始添加收藏夹，请选择收藏夹，然后选择“在资源中显示兼容的预设”，以查看可用路径预设的完整列表。

要收藏某个预设，请在“资源”面板或“属性”面板的“预设”部分中右键单击该预设，然后选择“添加到收藏夹”。 

还可以从收藏夹列表中移除预设。 右键单击已收藏的预设，然后选择“从收藏夹中移除”。

![选择路径工具时，“属性”面板的“预设”部分的屏幕截图。 选中了“收藏夹”选项，并突出显示了“在资源中显示兼容的预设”按钮。](../../assets/ShowCompatiblePresets.png){width="400px"}

### 创建路径预设

与其他工具一样，可以创建预设以快速恢复画笔设置/配置。 为此，只需在<b>属性</b>窗口中右键单击，然后选择<b>创建工具预设</b>。 在<b>资源</b>窗口中选择后，此新创建的预设将自动切换到路径工具。
