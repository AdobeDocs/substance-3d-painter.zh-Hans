---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/features/uv-tiles/image-sequence.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中使用带有UV磁贴的图像序列进行动画纹理工作流程。
helpx_creative_field: ""
helpx_description: Painter > Features > UV Tiles > Image Sequence
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 图像序列
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8b892d2d6c9d0f1a3b5d9d3ab9b180a7c2770a83
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---


# 图像序列

图像序列是层架中分组为单个资源的图像集合。 图像根据其文件名中的特定图案分组在一起。

## 如何将图像作为序列导入

导入图像文件时，如果文件名与特定模式匹配，则会自动将其导入为序列。 如果导入的文件旁边有其他图像，则也会考虑这些图像。 因此，无需手动从序列中导入所有文件，只需选取第一个文件即可。

文件名匹配示例：

以下文件名将成功导入图像序列，因为它们可以识别文件名的最后一部分是指UDIM编号1032：

* file\_22.1032.jpg
* file\_22-223.1032.jpg
* file\_22-223-1032.jpg
* file\_22-223\_1032.jpg

下列文件名不能作为图像序列导入，因为它们没有正确的结构化：

* file\_22-2232032.jpg
* file\_22-223PM2032.jpg
* file\_22-223-0032.jpg
* file\_22-223\_Rec2020.jpg

文件名匹配基于以下正则表达式：

```
 ^(.+?)[\.\-\_](?
```


## 如何使用图像序列

像加载任何其他资源一样，可以将图像序列加载到接口中的任何资源插槽中。 但在某些情况下，可能需要正确使用其他设置。

在[填充图层](../../painting/fill-projections/fill-projections.md)（和填充效果）中，确保投影模式设置为&#x200B;**填充（每个UV图块匹配）**，以确保将序列中的每个图像分配给纹理集中的右侧[UV图块](uv-tiles.md)。
