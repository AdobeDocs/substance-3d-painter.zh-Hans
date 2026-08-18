---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/features/effects/compare-mask.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中使用比较蒙版效果根据纹理比较操作创建蒙版。
helpx_creative_field: ""
helpx_description: Painter > Features > Effects > Compare Mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 比较蒙版
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 0%

---


# 比较蒙版

![](../../assets/compare-mask.png)

此效果允许快速轻松地比较两个通道并生成蒙版。 此效果仅适用于图层上的蒙版。

以下是此效果的可用设置：

| 设置 | 描述 |
| --- | --- |
| **频道** | 用于比较源和目标之间以创建蒙版的通道。 此列表基于[纹理集设置](../../interface/texture-set/texture-set-settings.md)中可用的通道。 |
| **比较** | 这里有三个参数可用于选择应如何计算蒙版。 中间的下拉菜单定义比较操作（小于、在公差范围内、大于）。 <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/compare-mode.png"/></div> 源模式和目标模式为：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>下方图层</strong> ：考虑当前图层下方所有图层的拼合版本。</li><li data-preserve-html="true"><strong>此图层</strong> ：仅考虑此图层。</li><li data-preserve-html="true"><strong>此蒙版</strong> ：考虑蒙版的现有内容（例如，如果填充效果或生成器效果已经存在）。</li><li data-preserve-html="true"><strong>常量</strong> ：统一值。</li></ul>操作包括：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>小于</strong> ：如果源（左侧下拉菜单）的值小于目标（右侧下拉菜单）的值，则将在蒙版中输出白色值。</li><li data-preserve-html="true"><strong>在容差范围内</strong> ：如果源（左侧下拉菜单）与目标（右侧下拉菜单）具有相似的值，则将在蒙版中输出白色值。</li><li data-preserve-html="true"><strong>大于</strong> ：如果源（左侧下拉菜单）的值高于目标（右侧下拉菜单）的值，则将在蒙版中输出白色值。</li></ul> |
| **常量** | 比较设置设为“常量”时要比较的值。 |
| **硬度** | 控制生成的蒙版比较的Smoothness/硬度。 |
| **源通道直方图** | 提供源和目标的直方图视图。 有助于了解它们是否重叠了一点（如果它们没有重叠，蒙版将为空）。有关直方图工作方式的更多信息，请参阅： [色阶](https://experienceleague.adobe.com/en/docs/substance-3d-designer/using/substance-graphs/nodes-reference-for-substance-graphs/atomic-nodes/levels)。 |

>[!NOTE]
>
> 可以右键单击图层并选择快捷方式“**使用Height组合添加蒙版**”以在图层上快速添加此新效果。 此快捷键还会将Height通道&#x200B;**混合模式**&#x200B;切换为“**正常**”，而不是默认的“**线性减淡（添加）**”。\
> ![](../../assets/compare-shortcut.png)
