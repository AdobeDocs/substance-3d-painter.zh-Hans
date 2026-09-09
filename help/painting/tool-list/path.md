---
helpx_url: 'https://helpx.adobe.com/cn/substance-3d-painter/painting/tool-list/path.html'
breadcrumb-title: ''
description: 使用Substance 3D Painter中的“路径”工具创建和编辑路径，以便精确绘制纹理和放置描边。
helpx_creative_field: ''
helpx_description: Painting > Path tools list > Path tool
helpx_experience_level: ''
helpx_learn_topic: ''
helpx_tags: ''
title: 路径工具概述
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6fcf10add7086a0e2a070ee6046c0a261ef1ae34
workflow-type: tm+mt
source-wordcount: '1666'
ht-degree: 0%

---


# 路径工具概述

![显示鞋子上使用的路径工具的图像](../../assets/v90_banner_path.jpg)

**路径工具**&#x200B;允许您定义一条带有路径曲面上点的曲线。网格工具包含多个点。 创建曲线后，不同的“路径”工具允许您沿着曲线创建不同的效果。

## 创建路径

可以在绘画图层和绘画效果上创建路径。 有两种方法可访问路径工具：

* **通过界面**：导航到左侧的工具工具栏，然后单击顶部的第三个图标。
* **通过键盘快捷键**：默认情况下，未为该工具分配任何资源。 可通过编辑“沿路径选择绘画”快捷键，在“设置”菜单中对此进行更改。

选择该工具后，可通过单击3D视口内的3D模型曲面来放置点。 创建路径至少需要两个点（或顶点）。

![显示路径工具的选择以及点的创建的Gif](../../assets/path_create_points.gif)

“路径”工具具有多种模式，它们可能与应用程序中提供的其他绘画工具类似：

* 沿路径绘制：沿定义的路径绘制常规画笔描边。
* [功能区路径](ribbon-tool.md)：沿路径绘制重复或拉伸的图像。
* [填充路径](filled-path.md)：使用统一颜色填充路径的内部。
* 沿路径擦除：绘制沿定义路径擦除/删除信息的描边。
* 沿路径涂抹：绘制沿定义路径涂抹/模糊信息的描边。

![显示不同路径工具模式的工具工具栏的屏幕截图](../../assets/PathTools.png)

例如，**涂抹**&#x200B;模式下的路径工具会影响其他绘画信息：

![在涂抹模式下显示路径工具的Gif](../../assets/v90_path_smudge.gif)

>[!NOTE]
>
> **路径工具**&#x200B;仅在几何图形表面的3D空间中工作。 当前不支持在UV空间中或作为屏幕空间投影创建路径。

### 编辑路径

路径点（或顶点）自动附着在网格表面。 它们可以随时移动和调整。 通过单击直线上的任意位置，可将新顶点添加到现有路径中。

* 按&#x200B;**Escape**&#x200B;或&#x200B;**Enter**&#x200B;将退出路径编辑。
* 退出后，单击网格的空白表面将开始一条新路径。
* 将鼠标悬停并单击现有路径即可将其选中，从而允许继续或编辑该路径。 也可以通过&#x200B;**路径**&#x200B;面板重新选择路径（请参阅下文）。

![显示路径上新点添加和现有点移动的Gif](../../assets/path_edit_move_points.gif)

某些属性是特定于作为一个整体的路径。 在&#x200B;**属性**&#x200B;窗口中找到的选项就是这种情况。 就像使用常规描边一样（请参阅[绘画工具文档](paint-brush.md)），可以定义路径的以下属性：

* **画笔**
* **Alpha**
* **材质**

**画笔**&#x200B;部分包含仅适用于“路径”工具的其他选项：

| **设置** | **描述** |
| --- | --- |
| **投影深度** | 确定路径需要离网格表面多近才能显示画笔图章。 若要直接在视口中查看此视觉反馈，可以在&#x200B;**路径显示设置**&#x200B;中启用&#x200B;**法线**（请参阅下文）。 |
| **向上轴** | **跟随路径**&#x200B;关闭时用于定向画笔图章的轴。   在有些情况下，让所有图章沿全球轴/方向而不是沿路径对齐更有意义。 例如，在金属表面上使用铆钉。 |

其他属性按路径上的点(顶点)定义，例如压力。 要编辑特定点，只需单击它（或使用矩形选区）。 然后使用上下文工具栏编辑选定的点值。

![显示每个顶点的压力版本的Gif](../../assets/path_point_pressure_example.gif)

### 控制正切

有时，平滑路径并不理想，可能是因为它不遵循3D模型的最佳表面，也可能是因为它不适合特定的外观。 为了解决这些问题，可以修改给定顶点的切线。 正切是控制路径弯曲方式的点的方向。

要在平滑或线性/断开切线之间切换，只需双击顶点（或使用上下文工具栏中的专用按钮）：

![显示如何控制正切上的Gid](../../assets/path_break_tangents.gif)

要更精确地控制正切的方向，请使用上下文工具栏中的“自定义正切”按钮手动覆盖它们：

![显示如何控制正切上的Gid](../../assets/path_control_tangents.gif)

如果点尚未移动，请使用&#x200B;**ALT**&#x200B;键盘快捷键在移动时中断正切。

使用&#x200B;**CTRL**&#x200B;键盘快捷键可同时缩放两个正切。

>[!NOTE]
>
> 正切控件沿与路径中给定点的法线对齐的计划定义。 这意味着正切不能在某些方向弯曲。

### 上下文工具栏

![路径模式下上下文工具栏的屏幕截图](../../assets/path_contextual_toolbar_overview.png)

选择&#x200B;**路径**&#x200B;工具时的&#x200B;**上下文工具栏**&#x200B;提供多种设置，可让您控制当前选定的路径：

<table>
  <tr>
    <th><strong>参数</strong></th>
    <th><strong>描述</strong></th>
  </tr>
  <tr>
    <td><strong>显示/隐藏视口界面</strong><br><img src="../../assets/path_contextual_toolbar_showhide.png" alt="路径工具显示隐藏图标"/></td>
    <td>如果启用，路径和顶点叠加将在视口中可见。</td>
  </tr>
  <tr>
    <td><strong>显示设置</strong><br><img src="../../assets/path_contextual_toolbar_display.png" alt="“路径显示设置”图标"/></td>
    <td>在视口中控制路径视觉反馈的外观：<br><ul><li><strong>手柄大小</strong>：控制路径点的尺寸。</li><li><strong>路径宽度</strong>：控制路径线的Thickness。<br></li><li><strong>路径颜色</strong>：控制路径线的颜色。<br></li><li><strong>未选择的路径颜色</strong>：控制非活动路径的颜色。<br></li><li><strong>法线</strong>：如果启用，则在路径的每个点上显示投影方向。<br></li><li><strong>正切</strong>：如果启用，则显示路径控制点的曲线方向。<br></li><li><strong>路径方向</strong>：如果启用，则在路径末尾显示一个小箭头，以指示其绘画方向。 这对于了解描边中的图章的定向非常有用。</li></ul><br><img src="../../assets/path_contextual_toolbar_display_settings.png" alt="路径显示设置面板的屏幕截图"/></td>
  </tr>
  <tr>
    <td><strong>反转路径方向</strong><br><img src="../../assets/path_contextual_toolbar_direction.png" alt="“反向路径方向”图标"/></td>
    <td>翻转当前路径的方向。 方向定义了用于在描边中绘画图章的常规方向。 反转路径有助于重新定向绘制的图案。</td>
  </tr>
  <tr>
    <td><strong>切换边角/平滑</strong><br><img src="../../assets/path_contextual_toolbar_smoothcorner.png" alt="切换平滑角图标"/></td>
    <td>断开或对齐当前所选顶点的正切，从而可在平滑曲线或线性曲线之间切换。<br><img src="../../assets/path_smooth_corner_demo.png" alt="同时具有平滑路径和线性路径的屏幕快照 "/><br><strong>注意：</strong>直接双击路径上的点也可以完成在边角/平滑行为之间切换。</td>
  </tr>
  <tr>
    <td><strong>自定义正切</strong><br><img src="../../assets/path_icon_custom_tangents.png" alt="自定义正切的路径工具图标"/></td>
    <td>如果启用，则允许手动控制路径上给定点的切线。<br><img src="../../assets/paht_cutom_tangents_demo.png" alt="显示自定路径正切的图像"/></td>
  </tr>
  <tr>
    <td><strong>开放/闭合路径</strong><br><img src="../../assets/path_contextual_toolbar_close.png" alt="开放闭合路径图标"/></td>
    <td>打开或关闭当前路径。 要闭合路径，需要首先选择当前路径的两个端点之一。<br><img src="../../assets/v90_path_open_close.gif" alt="显示路径打开然后闭合的Gif"/></td>
  </tr>
  <tr>
    <td><strong>删除顶点</strong><br><img src="../../assets/path_contextual_toolbar_delete.png" alt="删除路径顶点的图标"/></td>
    <td>删除路径上当前选定的顶点。</td>
  </tr>
  <tr>
    <td><strong>对称</strong><br><img src="../../assets/path_contextual_toolbar_symmetry.png" alt="对称功能的图标"/></td>
    <td>启用或禁用当前路径的对称性。 有关详细信息，请参阅<a href="../symmetry/symmetry.md">对称文档</a>。<br><img src="../../assets/v90_path_symmetry.gif" alt="显示正在对称中绘制的路径的Gif"/></td>
  </tr>
  <tr>
    <td><strong>隐藏/忽略排除的几何</strong><br><img src="../../assets/path_contextual_toolbar_exclude.png" alt="几何蒙版排除功能的图标"/></td>
    <td>如果启用，则使当前路径通过隐藏几何绘画。 有关详细信息，请参阅<a href="../../interface/layer-stack/geometry-mask.md">几何蒙版文档</a>。</td>
  </tr>
</table>

### “路径”面板

![路径面板](../../assets/path_panel_visibility.png)

>[!NOTE]
>
> 如果当前工具不是路径工具或者选择了填充图层/文件夹，则会隐藏面板。

视区内部是&#x200B;**路径**&#x200B;面板，其中列出了当前选定的绘画图层/效果的所有路径。 它提供了一种选择和管理路径的简单方法。

使用此面板，可以：

* 双击路径以&#x200B;**重命名**&#x200B;它。
* 通过选择路径，然后按Delete键，**删除**。
* **复制**/**粘贴**/**复制**&#x200B;具有专用键盘快捷键的路径。
* 使用眼睛图标&#x200B;**显示**&#x200B;或&#x200B;**隐藏**&#x200B;路径（控制路径是否应用于纹理化）。

为方便起见，还可以右键单击路径以打开提供相同操作的上下文菜单：

![路径面板右键单击菜单](../../assets/path_panel_rightclick_menu_copy_properties.png)

右键单击菜单还可打开操作以将路径的属性或位置复制到另一路径上。 这样可以轻松在不同路径之间共享或同步功能：

![显示如何复制和粘贴路径属性的Gif](../../assets/path_copy_paste_properties.gif)![显示如何复制和粘贴路径位置的Gif](../../assets/path_copy_paste_vertices.gif)

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

与其他工具一样，可以创建预设以快速恢复画笔设置/配置。 为此，只需在&#x200B;**属性**&#x200B;窗口中右键单击，然后选择&#x200B;**创建工具预设**。 在&#x200B;**资源**&#x200B;窗口中选择后，此新创建的预设将自动切换到路径工具。