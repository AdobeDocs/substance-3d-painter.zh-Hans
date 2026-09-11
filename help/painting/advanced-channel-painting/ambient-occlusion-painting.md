---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/painting/advanced-channel-painting/ambient-occlusion-painting.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中直接绘画ambient occlusion地图，向纹理添加逼真的阴影和深度。
helpx_creative_field: ""
helpx_description: Painter > Painting > Advanced channel painting > Ambient Occlusion Painting
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ambient occlusion绘画
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---


# ambient occlusion绘画

环境遮蔽通道允许在对象的环境阴影中绘制细节。 它可用于添加来自材料的AO详细信息，或者在需要时仅手动修复烘焙错误。

&#x200B;>> 

在计算机图形学中，ambient occlusion是一种用于计算场景中每个点与环境光照的公开程度的着色和渲染技术。 管子的内部通常比公开的外表面更被遮盖（因此更暗），并且管子内部越深，照明变得越被遮盖（且更暗）。 ambient occlusion可视为为每个表面点计算的辅助功能值。\
资料来源：&lt;https://en.wikipedia.org/wiki/Ambient_occlusion>

此计算的&#x200B;**结果**&#x200B;存储在名为“Ambient occlusion”映射的位图中。 可以在应用程序中直接烘焙此映射，请参阅： [烘焙](../../baking/baking.md)。

## 绘制环境遮蔽

要绘画自定义遮蔽详细信息，需要Ambient occlusion渠道。 可以通过[纹理集设置](../../interface/texture-set/texture-set-settings.md)添加它：

![](../../assets/add-ao-channel.png)

将通道添加到纹理集后，任何图层都可用于绘制新信息。 由于AO通道仅包含灰度信息，因此推荐的混合模式为&#x200B;**正常**（绘画结束）和&#x200B;**正片叠底**（合并）。

要详细了解这些混合模式以及如何按通道更改它们，请参阅： [混合模式](../../interface/layer-stack/blending-modes.md)。

## 在环境遮蔽上绘制附加映射

在某些情况下，在烘焙的Ambient occlusion上绘画可能会很有用，以便隐藏详细信息甚至修复烘焙问题。

Substance 3D Painter中项目的默认设置将Ambient occlusion **通道**&#x200B;与&#x200B;**其他映射**&#x200B;中的Ambient occlusion映射合并。 这意味着在默认情况下，无法在烘焙的附加地图上进行绘制，每个地图（已烘焙贴图和频道）的结果将相乘。 但是，此设置可通过以下设置进行更改：

### 1 — 添加Ambient occlusion渠道

在当前纹理集中添加ambient occlusion声道：\
![](../../assets/edit-ao-channel-optimized.gif)

将其混合模式设置为“**替换**”，而不是“**乘**”：\
![](../../assets/ao-mix-mode.gif)

### 2 — 使用烘焙的ambient occlusion设置填充图层

创建一个新填充图层，并通过“属性”面板将烘焙的ambient occlusion放在“ambient occlusion”插槽中。 如果填充图层的默认字幕尚未设置为1，请不要忘记将其更改。\
![](../../assets/ao-stack.png)

### 3 — 更改填充图层混合模式

默认情况下，任何新图层上的AO通道的混合模式设置为“**正片叠底**”。 由于最好使用填充图层作为基色，因此我们选择了“正常”混合模式，因为位图没有任何Alpha，它将替换下面的所有内容（包括着色器的默认颜色）。\
![](../../assets/ao-blend-mode.gif)

### 4 — 创建图层以绘画在烘焙的ambient occlusion图上

创建一个新图层（常规或填充），并将其混合模式更改为“正常”（对于AO通道）。 完成此设置后，AO通道上绘制的任何内容都将接管下面图层上烘焙的AO映射。\
![](../../assets/paint-over-ao-optimized.gif)
