---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/painting/advanced-channel-painting/normal-map-painting.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中直接绘制正常映射，向纹理添加表面细节和深度。
helpx_creative_field: ""
helpx_description: Painter > Painting > Advanced channel painting > Normal Map Painting
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 法线图绘画
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 0%

---


# 法线图绘画

绘制细节可以通过直接在网格上绘制法线图数据来完成。 此页面将用不同的方法来管理正常地图绘画。

## 绘画法线图详细信息

要法线图详细信息：

1. 在当前纹理集中添加常规通道（如果尚未存在）
1. 在当前绘画工具中启用正常通道
1. 在当前绘画工具的材料部分的“正常”槽中加载“正常”资源。

从此以后，使用法线映射绘画非常类似于[Height映射绘画](height-map-painting.md) ，并且增加了烘焙法线的精度。

![](../../assets/normal-painting.gif)

## 正常混合模式

法线图在图层堆叠中有自己的混合模式：

* **法线图详细信息**（默认）
* **法线图的反向详细信息**
* **法线图合并**

要了解这些模式，请参阅[混合模式](../../interface/layer-stack/blending-modes.md)页面。

## 标准色彩空间

将法线映射载入素材槽（工具属性或填充图层）时，可以更改默认色彩空间。

此设置可用于指定法线贴图格式，因为默认情况下应为DirectX(Y-)法线图（不受项目设置的影响）。 因此，使用OpenGL (Y+)法线图时，需要单击小箭头以打开色彩空间菜单，然后更改位图的色彩空间。

![](../../assets/normal-color-space.png)

## 在烘焙的法线图上绘画

在某些情况下，为了隐藏详细信息（甚至修复烘焙问题），能够绘画烘焙的法线图会很有用。\
Substance 3D Painter中项目的默认设置不允许这样做，因为它单独计算正常声道和烘焙的正常声道。 此行为可以通过[纹理集设置](../../interface/texture-set/texture-set-settings.md)进行更改。

### 1 — 更改纹理集混合模式

默认情况下，将使用设置为&#x200B;**合并**&#x200B;的&#x200B;**正常混合**&#x200B;设置创建纹理集。

若要覆盖/法线图，请务必将此设置设置为&#x200B;**替换**。 法线图将从视口中消失，但这是可预期的。 将此模式更改为&#x200B;**replace**&#x200B;指示Substance 3D Painter在生成最终法线图时仅考虑正常声道和Height声道。

![](../../assets/normal-mixing.png)

### 2 — 使用烘焙的法线图设置填充图层

创建一个新填充图层，并通过“属性”面板将烘焙的正常内容放入“正常”插槽中。 如果填充图层的默认字间距未设置为1，请不要忘记将其更改。

![](../../assets/fill-layer_1.gif)

### 3 — 更改填充图层混合模式

默认情况下，任何新图层上正常声道的混合模式都设置为“法线图细节”。 由于最好使用填充图层作为基色，因此我们选择了“正常”混合模式，因为位图没有任何Alpha，它将替换下面的所有内容（包括着色器的默认颜色）。

![](../../assets/blending-mode.gif)

### 4 — 创建图层以绘画在烘焙的法线图上

创建一个新图层（常规或填充），并将其混合模式更改为常规通道的“正常”。 完成此设置后，在正常通道上绘制的任何内容都将取代下方图层上的法线图。

![](../../assets/normal-painting-over.gif)
