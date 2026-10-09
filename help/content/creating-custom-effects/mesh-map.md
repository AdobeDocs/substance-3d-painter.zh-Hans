---
breadcrumb-title: ""
description: 了解如何使用Substance 3D Painter自定义效果中的网格图来访问基于几何的纹理信息。
title: 网格图
user-guide-description: ""
user-guide-title: ""
source-git-commit: 6b6d52207ca1d043aaa1b2b14145b6b49d4c1942
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 3%
---

# 网格图

要在图层上添加效果时自动连接网格图（烘焙的纹理），必须遵循特定的命名约定。

>[!NOTE]
>
> 可以在输入节点中使用&#x200B;**用法**&#x200B;或&#x200B;**标识符**（用法具有优先级）。

以下是每个网格图的命名约定：

| 网格图 | 使用情况 | 标识符 |
| --- | --- | --- |
| *Ambient occlusion* | **ambientOcclusionBase** | **环境\_遮蔽** |
| *ID* | **id** | **id** |
| *弯曲* | **弯曲** | **弯曲** |
| *正常* | **normalBase** | **normal\_base** |
| *世界空间法线* | **正常WS** | **world\_space\_normals** |
| *位置* | **位置** | **位置** |
| *Thickness* | **Thickness** | **Thickness** |
| *Height* | **heightBase** | **Height\_base** |
| *Bent normals* | **bentNormalsBase** | **bent\_normals\_base** |
| *不透明度* | **不透明度基数** | **不透明度\_base** |
