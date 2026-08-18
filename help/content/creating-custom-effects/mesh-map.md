---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/content/creating-custom-effects/mesh-map.html"
breadcrumb-title: ''
description: 了解如何在自定义效果中使用网格图，以便Substance 3D Painter访问基于几何的纹理信息。
helpx_creative_field: ""
helpx_description: Painter > Content > Creating custom effects > Mesh Map
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 网格图
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 3%

---


# 网格图

要在图层上添加效果时自动连接网格图（烘焙纹理），必须遵循特定的命名约定。

>[!NOTE]
>
> 可以在输入节点中使用&#x200B;**用法**&#x200B;或&#x200B;**标识符**（用法具有优先级）。

以下是每个网格映射的命名约定：

| 网格图 | 使用情况 | 标识符 |
| --- | --- | --- |
| *环境遮蔽* | **ambientOcclusionBase** | **环境\_遮蔽** |
| *ID* | **id** | **id** |
| *曲率* | **曲率** | **曲率** |
| *正常* | **normalBase** | **normal\_base** |
| *世界空间法线* | **正常WS** | **world\_space\_normals** |
| *位置* | **位置** | **位置** |
| *Thickness* | **Thickness** | **Thickness** |
| *Height* | **heightBase** | **Height\_base** |
| *弯曲法线* | **bentNormalsBase** | **bent\_normals\_base** |
| *不透明度* | **不透明度基数** | **不透明度\_base** |
