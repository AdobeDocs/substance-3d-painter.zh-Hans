---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/painting/dynamic-strokes/dynamic-stroke-performances.html"
breadcrumb-title: ''
description: 了解Substance 3D Painter中的动态笔触性能注意事项，以优化画笔笔触渲染和响应。
helpx_creative_field: ""
helpx_description: Painter > Painting > Dynamic strokes > Dynamic Stroke Performances
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 动态描边性能
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '995'
ht-degree: 0%

---


# 动态描边性能

对于动态笔触来说，Substance图表的性能非常重要，因为Substance可以在很短的时间内多次再生。 如果Substance计算太重，则可能会造成延迟，因此会在绘画时断断续续和冻结。 所有这些最终都会造成糟糕的绘画体验。 此页将有关使用“动态描边”功能的信息和建议重新分组。

## 动态笔触计算可能会很繁重

同样重要的是知道计算可以在不同的上下文中产生影响：

* **绘画时** ：绘画时生成动态描边（取决于其设置）。 错误配置可能会使绘画变慢和滞后。
* **重新打开项目时** ：即使绘画过程顺利完成，打开项目时仍有可能出现计算停滞，从而使打开项目的时间比平常长得多。 这是因为最初的绘画过程进展顺利，因为计算会随着时间的推移而扩散，然而打开项目时几乎都会同时进行。 这意味着，如果未正确配置动态描边，项目可能会请求生成数千个唯一的Substance。
* **内存消耗** ：为Substance图生成大量变化可能会消耗大量内存（因为这些生成在运行时会变得不稳定）。

## 使用抖动和间距设置

虽然在Substance内实现令人印象深刻或高级的效果很容易，但保持简单并使用Substance 3D Painter刀具参数的本机设置，有时可能更为有利。 绘画引擎的计算速度要快得多：

* **抖动** ：这些参数允许通过更改某些属性而不重新计算Substance（例如角度、位置和不透明度）以非常低成本创建随机性。
* **间距** ：间距越小，绘画描边时创建的图章就越多。 有时，不需要连续的画笔描边，使用较大的间距也可以帮助更好地查看使用的Alpha/素材。

## 何时以及使用哪种类型的随机

随机种子是生成唯一性的好方法。 问题在于，生成过程可能很耗费，而且在动态描边功能的情况下，如果不进行适当调整，生成过程可能会相当频繁。 了解何时使用随机种子以及何时避免使用随机种子非常重要，我们更喜欢使用其他方法以便在视觉效果和性能之间实现最佳平衡：

* **每图章随机植入** ：在这种情况下，将针对每个图章生成新的唯一Substance。 例如，这适用于在木板上创建独特的美甲，但是如果您要创建油墨/绘画轨迹，则不能这样做。
* **每个描边的随机植入** ：为当前画笔描边创建唯一的随机植入。 当图章较少但需要具有每个描边的新变化集（如喷涂效果）时，此效果非常有用。
* **静态随机植入** ：Substance生成过一次，且永远不会更改。 最适合表演，但可能过于局限，具体取决于您的需求。

**时间** ($time)是什么？\
时间可能有助于创建一些非常具体的外观，但实际上它是在Substance图中使用的最昂贵的变量之一。 这是因为很难获得画笔描边与画笔描边之间的相似值，因此画笔引擎可能会随时产生新的变化。 如果可以，请避免使用空格，并改用图章索引，二者结合使用可能会得到类似的结果。

## StampIndex和StampCycleCount用法

**StampIndex**&#x200B;是画笔描边中单个图章的ID。 默认情况下，它从0开始，每个新图章增加1。 **StampCycleCount**&#x200B;用于限制唯一索引的数量，并告知Substance 3D Painter回收/重用已生成的Substance图表。 当当前ID达到限制时，Substance 3D Painter将从0重新开始，从而创建循环。

因此，在保持良好性能的同时具有随机性的最佳解决方案是使用以下循环盘点：

* **StampIndex as RandomSeed** ：创建Substance图时，可以将随机植入设置为绝对。 通过执行此操作，您可以为其提供一个自定义值，该值可以是图章索引。 这将为笔触内的每个图章创建一个独特的Substance图形版本。
* **与StampCycleCount**&#x200B;相结合：您实际上可以创建一组有限的新变体，然后重新使用它们。
* **随机启动** ：如果将周期盘点设置为从随机值而不是0开始，则意味着它将对已生成图形池内的每个描边在开始处获取不同的Substance版本。

## 禁用基于参数值的计算

Substance 3D Painter无法确定何时调整某个参数以生成相同的输出，原因很简单，就是计算隐藏在Substance图中。 这基本上是一个黑盒子。

为了在调整参数和使用动态笔触绘画时提高性能，可以通过使用Substance图形的userdata字段中的条件值来指定何时生成新的图形实例。

可能的值为：

| *变量* | *用法* |
| --- | --- |
| **IsStampIndexActive** | 用于确定在绘画过程中图章索引是否应更改。 |
| **IsRandomSeedActive** | 用于确定随机植入是否应在绘画过程中更改。 |
| **IsTimeActive** | 用于确定在绘画期间时间($time)是否应递增。 |

例如：

```
IsRandomSeedActive=input.roundness_jitter>0 || input.flip_x_jitter || input.flip_y_jitter
```


在这种情况下，仅当图形参数（标识符） **圆度\_jitter**&#x200B;大于0，或者启用了布尔型&#x200B;**翻转\_x\_jitter**&#x200B;或&#x200B;**翻转\_y\_jitter**&#x200B;时，才会更改随机植入。 如果不满足该条件，则不会重新生成图形。 图形参数的前缀必须为“**输入。**”  ”以待识别。
