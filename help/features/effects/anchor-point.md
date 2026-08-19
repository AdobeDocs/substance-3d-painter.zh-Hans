---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/features/effects/anchor-point.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中使用锚点效果来引用其他图层中的纹理以实现高级合成。
helpx_creative_field: ""
helpx_description: Painter > Features > Effects > Anchor Point
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 锚点
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 0%

---


# 锚点

锚点是一种公开图层栈栈中的任何资源或元素的方法，出于不同目的并通过一组不同的调整在图层栈栈的不同区域中引用它。 它们提供了一组全新的可能性，允许您有效地将图层或蒙版链接到一起，并让单个锚点影响项目的多个方面，从而将Substance 3D Painter转变为真正的非线性体验。

>[!NOTE]
>
> 锚点只能在创建的同一纹理内引用。 不能跨纹理集创建锚点与其引用之间的链接。

## 添加锚点

锚点在“效果”菜单中可用。 它们可以添加到图层和蒙版上。

![](../../assets/add-anchor-point.png)

## 使用锚点作为参考

一个锚点可以被另一个图层引用：这将把锚点的内容实例化到引用它的图层中。

锚点可在以下资源中用作参考：

* 填充图层
* 填充效果
* Substance滤镜的输入（效果、过程、生成器）

![](../../assets/anchor-point-resource.png)

只有位于&#x200B;**下方**&#x200B;且引用它的图层的锚点才能用作引用。\
如果将锚点移动到引用它的图层上方，它将中断引用。 如果要取消此操作，则可以撤消。

![](../../assets/layer-broken.png)![](../../assets/reference-broken.png)

## 查找锚点的引用

单击锚点时，您可以在属性中看到此锚点用作引用的图层列表。

![](../../assets/references.png)

## 查找锚点

如果您是使用锚点作为参考的填充图层/效果，则可以跳转到锚点。

![](../../assets/jump-to-anchor-point.png)
