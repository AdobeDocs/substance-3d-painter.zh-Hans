---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/interface/texture-set/texture-set-list.html"
breadcrumb-title: ''
description: 了解如何使用Substance 3D Painter中的纹理集列表管理和整理项目中的多个纹理集。
helpx_creative_field: ""
helpx_description: Painter > Interface > Texture Set > Texture Set list
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 纹理集列表
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 0%

---


# 纹理集列表

![](../../assets/texture-set-list.png)

**纹理集列表**&#x200B;窗口显示项目中当前3D模型的所有材料ID。 它允许切换和查看与模型上每个材料关联的图层堆叠及其专用设置。

“纹理集列表”窗口的主要目标是允许从一个材料切换到另一个文档，以访问与每个材料关联的图层堆叠。\
对于[材料分层](../../features/dynamic-material-layering.md)工作流，**子堆叠**&#x200B;在纹理集名称&#x200B;**下方**&#x200B;显示。

>[!WARNING]
>
> 一次只能编辑/绘制一个纹理集。

## 纹理集状态

纹理集可能具有多个状态：

![](../../assets/txtset-status.png)

* **已选择** ：当前正在编辑当前纹理集。 选择纹理集将相应地更新[图层堆叠](../layer-stack/layer-stack.md)和[着色器设置](../shader-settings/shader-settings.md)窗口。
* **可见/隐藏** ：有关更多详细信息，请参阅下面的可见性部分。
* **已禁用** ：这意味着无法将纹理集及其关联图层堆叠附加到网格上的材料。 有关详细信息，请参阅[纹理集重新分配](texture-set-reassignment.md)。

## 可见性

![](../../assets/texturesetlist.png)

可通过专用图标来显示纹理集：

| *图标* | *操作* | *描述* |
| --- | --- | --- |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/txtsetlist-icon-menu.png"/></div> | 打开菜单 | 打开包含以下操作的新菜单：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>显示全部</strong>：将显示视口中的所有纹理集。</li><li data-preserve-html="true"><strong>全部隐藏</strong>：将隐藏视口中的所有纹理集。</li><li data-preserve-html="true"><strong>反转显示/隐藏</strong>：可见纹理集将变为隐藏，隐藏纹理集将变为可见。</li></ul> |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/txtsetlist-icon-isolate.png"/></div> | 焦点模式 | 在此模式处于活动状态时，隔离当前活动的纹理集并隐藏所有其他文档。 再次单击此按钮以退出模式。 |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r3-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/txtsetlist-icon-visible.png"/></div> | 可见性 | 单击纹理集旁边的此按钮，可在视口中隐藏或显示纹理集。 |

>[!NOTE]
>
> 默认情况下，**绘画**&#x200B;时仅显示正在选择的纹理集。 可以通过取消选中“**仅在绘画**&#x200B;时显示选定的材料”，在[首选项](../settings/settings.md)中更改此行为。\
> 注意：在绘制&#x200B;**改善性能**&#x200B;时隐藏其他纹理集。

## 上下文菜单

![](../../assets/txtset-list-contextualmenu.png)

右键单击纹理集名称时，将打开包含以下操作的上下文菜单：

* **显示/隐藏纹理集** ：切换纹理集的可见性（如上一节所述）
* **编辑名称** ：允许重命名纹理集。 在纹理导出过程中也将使用此名称。 也可以通过双击纹理集名称来重命名。
* **将名称重置为\*原始名称\*** ：如果原始的纹理集名已更改，请从网格材料还原它。
* **编辑描述** ：允许添加/更改与纹理集关联的描述。

## 着色器管理

每个纹理集名称右侧的按钮可用于管理着色器分配。\
默认情况下，每个纹理集共享相同的着色器实例。 但是，有时只对网格的特定部分使用其他着色器会很方便。 可通过单击该按钮并选择“**新建着色器实例**”来完成此操作。 在此处，可以在[着色器设置](../shader-settings/shader-settings.md)窗口中更改着色器及其参数，而不会影响其他纹理集。

![](../../assets/capture-d-e-cran-2018-07-12-a-15-45-32.png){width="500px"}

## 设置

设置按钮可打开一个公开多个操作的新菜单：

* **隐藏空说明**（默认） ：隐藏说明字段（如果为空）
* **隐藏所有说明** ：隐藏说明字段，即使不为空
* **显示所有描述** ：显示描述字段，即使该字段为空
* **导入着色器参数** ：允许导入json文件以配置纹理集的着色器参数
* **重新分配纹理集** ：有关详细信息，请参阅[纹理集重新分配](texture-set-reassignment.md)。
