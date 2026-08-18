---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/painting/dynamic-strokes/enabling-dynamic-stroke-feature.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中启用动态描边功能，以创建具有变量效果的响应式画笔描边。
helpx_creative_field: ""
helpx_description: Painter > Painting > Dynamic strokes > Enabling Dynamic Stroke Feature
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 启用动态笔触功能
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 2%

---


# 启用动态笔触功能

要启用动态笔触功能，首先需要特定资源。

## 查找动态笔触兼容资源

浏览[资源](../../interface/assets/assets.md)窗口时，缩览图右下角的专用图标指示了资源的兼容性类型。 如果没有图标可见，则表示资源无法利用该功能。

| *图标* | *描述* |
| --- | --- |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/icon-dyn.png"/></div> | 此资源可以使用以下一个或多个行为：<ul data-preserve-html="true"><li data-preserve-html="true">Stamp Index</li><li data-preserve-html="true">时间</li><li data-preserve-html="true">随机种子</li></ul> |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../assets/icon-random.png"/></div> | 此资源仅公开随机植入参数。 |

还可通过使用以下关键字使用架中的搜索字段来搜索资源：

* dynamicstroke
* 随机植入

## 动态笔触参数

![](../../assets/dynamic-strokes-settings.png)

加载动态描边资源后，新参数列表将紧靠在Substance参数组之前添加。

| *参数* | *描述* |
| --- | --- |
| **动态控件** | 列出当前使用的Substance文件可用的参数。 |
| **图章开始** | 仅当资源具有动态控件“图章索引”时才可用。 指示画笔描边内图章索引的起始值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>从开头(0)</strong>：默认值。 索引从每个新描边处的零开始。</li> <li data-preserve-html="true"><strong>来自随机索引</strong>：索引从随机值（其最大值由图章周期计数定义）开始。 请注意，以下值仍将按顺序排列，而非完全随机。</li> </ul> |
| **图章周期计数** | 仅当资源具有动态控件“图章索引”时才可用。 此参数控制Substance 3D Painter应在何时停止生成新的Substance变体并开始循环利用现有字体。 此参数对性能有很大的影响，您可以阅读有关[动态描边性能](dynamic-stroke-performances.md)的更多信息。 |
| **随机种子类型** | 仅当资源具有动态控件“随机植入”时才可用。 控制随机植入应如何更改：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>单个</strong>：默认值。 使用单个随机植入值，该值可通过Substance参数手动设置。</li> <li data-preserve-html="true"><strong>每个描边的随机</strong>：为每个新画笔描边生成新的随机种子值。</li> <li data-preserve-html="true"><strong>每图章随机</strong>：为画笔描边内的每个图章生成新的随机种子值。 <em><strong>请谨慎使用参数，因为它可能会非常昂贵</strong>。</em></li> </ul> |
| **时间** | 时间动态控件没有任何参数。 时间取决于画笔描边的绘画时间。 |

## 兼容工具列表

“动态描边”设置仅适用于以下工具和上下文：

| *工具类型* | *兼容的资源槽* |
| --- | --- |
| **绘画** | <ul data-preserve-html="true"><li data-preserve-html="true">Alpha</li><li data-preserve-html="true">材质</li></ul> |
| **橡皮擦** | <ul data-preserve-html="true"><li data-preserve-html="true">Alpha</li><li data-preserve-html="true">材质</li></ul> |
| **投影** | <ul data-preserve-html="true"><li data-preserve-html="true">Alpha</li></ul> |
| **涂抹** | <ul data-preserve-html="true"><li data-preserve-html="true">Alpha</li></ul> |
| **克隆** | <ul data-preserve-html="true"><li data-preserve-html="true">Alpha</li></ul> |

>[!NOTE]
>
> 动态笔触与&#x200B;**粒子**&#x200B;不兼容，这就是在物理模式下使用任何“工具”时该功能被禁用的原因。
