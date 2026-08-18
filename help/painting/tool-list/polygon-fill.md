---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/painting/tool-list/polygon-fill.html"
breadcrumb-title: ''
description: 使用Substance 3D Painter中的“Polygon Fill Tool”（多边形填充工具）为选定的多边形添加颜料以实现高效的纹理绘制。
helpx_creative_field: ""
helpx_description: Painter > Painting > Tool list > Polygon fill
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Polygon fill
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 1%

---


# Polygon fill

**多边形填充**&#x200B;工具(![](../../assets/image2018-6-12-18-15-12.png))允许您将选定的多边形转换为像素蒙版以快速绘制蒙版。 它可能看起来像来自其他3DCC应用程序的3D选择工具，但实际上是一种生成像素数据的绘画填充工具。 这意味着可以通过使用它来选择或取消选择黑色。

多边形填充工具在[绘画图层](../../interface/layer-stack/layer-stack.md)上起作用，但仅限于基色，不能用于此目的。 [仅将其用于蒙版](../../interface/layer-stack/masking-and-effects.md)。

它有4种选择模式：

* ![](../../assets/image2020-9-30-11-31-53.png) **三角形填充** — 填充单个网格三角形。
* ![](../../assets/image2020-9-30-11-32-12.png) **多边形填充** — 填充整个多边形。 如果您的网格在导出时已经进行三角化，则不会执行任何与“三角形填充”不同的操作。
* **![](../../assets/image2020-9-30-11-32-42.png)网格填充** — 填充整个连接的子网格。 就像3D应用程序中的“子对象”模式一样，将填充与所单击多边形相连的每个多边形。
* **![](../../assets/image2020-9-30-11-32-54.png)UV区块填充** — 填充整个UV区块或“岛”。 工作方式类似于网格填充，但需查看在UV空间中连接的多边形。 填充停止在UV边界。

![](../../assets/polygon-fill.gif)

这4种模式可以组合和切换，这意味着某些智能使用方式可让您使用网格和UV区块模式快速标记和取消标记蒙版中的部分。

与“多边形填充”工具关联的（默认）热键有：

* *数字键4* — 选择多边形填充工具。
* *X* — 绘画蒙版时反转当前颜色。 会迅速地把黑换白。 在材质绘制模式下，此热键无效。
