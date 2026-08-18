---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/content/creating-custom-effects/mesh-based-input.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter的自定义效果中使用基于网格的输入来创建几何识别纹理效果。
helpx_creative_field: ""
helpx_description: Painter > Content > Creating custom effects > Mesh Based Input
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 基于网格的输入
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 1%

---


# 基于网格的输入

基于网格的输入是由Substance 3D Painter引擎从当前项目内的网格中提取的纹理。 这些纹理可用于根据网格拓扑创建高级效果。

>[!NOTE]
>
> 这些Mesh信息基于拓扑本身，不考虑Mesh映射（烘焙纹理）。
> 
> 引擎提供的输入是32位浮点纹理，它将缩放/固定到Substance图中的输入值。

| 网格信息 | 标识符 | 使用情况 | 描述 |
| --- | --- | --- | --- |
| *位置(RGB)* | **mesh\_position** | **meshPosition** | 检索包含顶点位置的纹理。 |
| *世界空间正常(RGB)* | **mesh\_world\_space\_normal** | **meshNormalWS** | 检索包含世界空间中的顶点法线的纹理。 |
| *世界空间切线(RGB)* | **mesh\_world\_space\_tangent** | **meshTangentWS** | 检索在世界空间中包含顶点切线的纹理。 |
| *World Space Bitangent(RGB)* | **mesh\_world\_space\_bitangent** | **meshBitangentWS** | 检索世界空间中包含顶点双切线（双法线）的纹理。 |
| *文本大小（灰度）* | **mesh\_texel\_size** | **meshTexelSize** | 检索包含纹理大小（像素密度和网格UV之间的差异）的纹理。 |
| *UV蒙版（灰度）* | **网格\_uv\_蒙版** | **meshUVMask** | 将纹理检索为网格UV 岛的黑色（外部）和白色（内部）蒙版。 |
