---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/features/iray-renderer/iray-settings.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中配置Iray渲染器设置，以控制渲染质量和性能。
helpx_creative_field: ""
helpx_description: Painter > Features > Iray Renderer > Iray Settings
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 图像设置
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 0%

---


# 图像设置

![](../../assets/iray-settings.png)

“Iray”设置控制IRay视区的渲染、运行时间和质量。

## 图像信息

窗口顶部显示Iray的状态以及其他信息。

| *设置* | *描述* |
| --- | --- |
| **状态** | 该状态指示Iray的工作方式：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>正在渲染</strong> （Iray正在计算图像）</li><li data-preserve-html="true"><strong>已暂停</strong> （Iray计算已停止，但尚未完成）</li><li data-preserve-html="true"><strong>完成</strong>（Iray计算已完成，或达到设置值）</li></ul> |
| **分辨率** | Iray图像的分辨率（默认情况下取决于视口大小）。 |
| **场景大小** | 场景/3D网格的定界框大小。 没有单位，但假定有厘米。 |
| **迭代** | Iray在设置中定义的最大值范围内完成的计算遍数。 |
| **渲染时间** | 在设置中定义的最长时间内执行渲染所用的时间。 |

>[!NOTE]
>
> 迭代次数将定义渲染的最终品质：迭代次数越多，品质越好。\
> 但是，迭代可能需要一些时间，因此可以定义最长时间。 迭代由样本数定义。

## 设置

修改设置后，Iray将开始计算渲染。\
可以使用专用按钮暂停Iray以避免此行为：

![](../../assets/pause-2.png)

| *设置* | *描述* |
| --- | --- |
| **分钟样本** | 按像素执行的最小采样量 |
| **最大示例** | 按像素执行的最大采样量 |
| **最长时间** | Iray执行计算所允许的最大时间量。  右侧的下拉菜单允许设置设备（秒、分钟或小时）。 |
| **焦散Sampler已启用** | 此选项允许计算更高级的光照反射（焦散线）。 |
| **Firefly筛选器已启用** | 使用此选项可去除有时可能出现的孤立的非常明亮的像素。 |
| **覆盖视区分辨率** | 此设置允许定义渲染的自定义大小，而不是使用当前视区大小。 下面的&#x200B;**宽度**&#x200B;和&#x200B;**Height**&#x200B;设置允许以像素量定义宽度。 |
| **保存渲染** | 将当前渲染（即使未完成）导出到文件的操作。 |
| **共享** | 允许将当前渲染共享/导出到[ArtStation](https://www.artstation.com/)。 |
