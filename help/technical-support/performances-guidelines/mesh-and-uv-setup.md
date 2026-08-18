---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/technical-support/performances-guidelines/mesh-and-uv-setup.html"
breadcrumb-title: ''
description: 了解Substance 3D Painter中网格和UV设置的最佳实践，以优化性能和纹理质量。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Performances guidelines > Mesh and UV setup
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 网格和UV设置
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 0%

---


# 网格和UV设置

为Painter准备网格需要几分钟时间，这样可以更快、更轻松地完成纹理创建过程。

+++高多边形数模型
Painter可以处理的多边数没有特定的基准，因为它主要取决于机器规格、纹理集分配和图层栈叠属性，但如果考虑图层栈叠优化，则小于1000万个多边数应可以很好地处理。

+++

+++低多角数模型
有这么一个东西，多边形太低。 这是因为纹理引擎使用多边形来了解应渲染网格的哪个部分来计算画笔笔触。 具有极低多边形数的网格可以完全重新渲染，即使具有可能导致GPU不必要的过度工作的细小画笔描边也是如此。

例如，如果对单个四边形平面进行纹理化处理，则更应细分网格，尤其是在使用大量描边进行手绘时，因为信息会扩展到更多顶点。

+++

+++跨多个纹理集分割纹理
最好将具有较复杂材质分配的较大网格拆分为多个纹理集。 纹理集允许您为每个纹理集指定不同的设置，例如分辨率和着色器属性。 例如，如果仅网格的一部分使用半透明或SSS，则最好为该部分指定另一个“纹理集”和不同的着色器实例。 这样，这些更复杂的属性就不必在未使用的位置进行计算。

+++

+++保持UV 岛紧密相连
尝试将3D空间中的邻居UV 岛保持在一起。 这适用于UDIM布局和经典UV空间布局。 如果它们共享绘画描边或纹理工具，则当它们挤在UV空间的同一区域中时更容易计算它们，而不是当它们位于相对端时。

纹理引擎通过将纹理分割成较小的块来加快计算。 这意味着每个笔触仅更新需要更改的块，而不是使用每个笔触更新整个纹理。 通过将相邻UV 岛保持相互靠近，它将受单个描边影响的块数量减至最少。

+++

+++避免对象过多
在导入少于8000个子对象的网格时，性能应保持良好。 超过此限制可能会影响视区和绘画性能。 如果达到此限制，我们建议将对象合并在一起，以减少渲染开销。

+++
