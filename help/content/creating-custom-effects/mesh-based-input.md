---
breadcrumb-title: ""
description: 了解如何在Substance 3D Painter的自定义效果中使用基于网格的输入来创建几何识别纹理效果。
title: 基于网格的输入
user-guide-description: ""
user-guide-title: ""
source-git-commit: 6b6d52207ca1d043aaa1b2b14145b6b49d4c1942
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 1%
---

# 基于网格的输入

基于网格的输入是由Substance 3D Painter引擎从当前项目内的网格中提取的纹理。 这些纹理可用于根据网格拓扑创建高级效果。

>[!NOTE]
>
> 这些网格信息基于拓扑本身，不考虑网格图(烘焙纹理)。
> 
> 该引擎提供的输入是32位浮点纹理，其将被缩放/固定到Substance图形中的输入值。

| 网格信息 | 标识符 | 使用情况 | 描述 |
| --- | --- | --- | --- |
| *位置(RGB)* | **网格\_位置** | **meshPosition** | 检索包含顶点位置的纹理。 |
| *世界空间法线(RGB)* | **mesh\_world\_space\_normal** | **meshNormalWS** | 检索世界空间中包含顶点法线的纹理。 |
| *正切(RGB)* | **mesh\_world\_space\_tangent** | **meshTangentWS** | 检索世界空间中包含顶点正切的纹理。 |
| *世界空间Bitangent(RGB)* | **mesh\_world\_space\_bitangent** | **meshBitangentWS** | 检索世界空间中包含顶点双正切（双法线）的纹理。 |
| *文本大小（灰度）* | **网格\_texel\_size** | **meshTexelSize** | 检索包含纹理大小（像素密度和UV之间的差异）的纹理。 |
| *UV 蒙版（灰度）* | **网格\_uv\_蒙版** | **meshUVMask** | 将纹理检索为网格UV 岛的黑色（外部）和白色（内部）蒙版。 |
