---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/getting-started/export.html"
breadcrumb-title: ''
description: 了解如何从Substance 3D Painter导出各种格式的纹理以用于其他应用程序和游戏引擎。
helpx_creative_field: ""
helpx_description: Painter > Getting Started > Export
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 导出
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 1%

---


# 导出

## 导出纹理

纹理将作为位图集合导出。 得益于输出模板，Painter在导出纹理时提供了很大的灵活性。 使用输出模板，可以控制导出文件的名称、纹理打包到通道中的方式，以及导出文件的格式和位深度等内容。 如果这听起来令人望而生畏，别担心，Painter包含数十种默认输出模板，它们针对常用3D应用程序和用例进行了配置。

您打开<b>导出窗口</b>并开始使用<b>文件>导出纹理</b>导出纹理，或使用键盘快捷键<b>CTRL + SHIFT + E</b>。使用以下链接了解有关导出纹理的更多信息：

* [“导出”窗口](../export/export-window/export-window.md)
* [输出模板](../export/export-presets/export-presets.md)
* [修改或创建输出模板](creating-export-presets.md)

### 导出网格

Painter可以修改导入的网格，例如，通过自动生成UV。 如果已在Painter中对网格进行了更改，可以使用<b>文件>导出网格</b>导出网格。

导出网格时，您会看到一些选项：

* <b>无位移/镶嵌</b>：导出基础网格，而不修改基于素材的几何。
  * <b>应用三角化</b>：如果导入的网格由四边形或多边形组成，您可以启用此选项以导出Painter三角化版本的网格。 这有助于避免在其他应用程序进行不同的三角化时基于视觉三角化的错误。
* <b>使用位移/镶嵌</b>：Painter镶嵌网格，添加更多多边形，并使用位移或Height更改网格的表面几何。
  * <b>重新计算顶点法线</b>：修改网格的表面可能导致先前存在的顶点的法线不正确。 启用此选项后，Painter将自动更新顶点法线到新曲面的正确值。

![](../assets/export-render.jpg){width="500px"}
