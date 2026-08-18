---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/technical-issues/rendering-issues/mesh-flash-to-white-when-moving-camera.html"
breadcrumb-title: ''
description: 了解如何修复在Substance 3D Painter视口中移动相机时网格闪烁为白色的问题，以实现稳定渲染。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > Rendering Issues > Mesh flash to white when moving camera
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 移动相机时网格闪光灯变为白色
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---


# 移动相机时网格闪光灯变为白色

![](../../../assets/white-flash-svt-optim.gif){width="300px"}

当旧项目在视口中围绕相机移动时，可能会短暂显示由白色/空纹理创建的白色闪光灯。 这是因为[稀疏虚拟纹理](https://substance3d.adobe.com/display/DRAFTPAINTER/Sparse+Virtual+Textures) (SVT)系统依赖于特定着色器配置，而较旧的着色器不使用这些配置。

要去除白色闪光灯，只需&#x200B;**更新****项目着色器**：

* 对于&#x200B;**默认着色器**：按照[更新着色器](../../../interface/shader-settings/updating-a-shader.md)页面中的分步过程操作。
* 对于&#x200B;**自定义着色器**：查看日志中的错误消息以及[着色器 API](https://helpx.adobe.com/substance-3d/unlisted/documentation/spdoc/custom-shader-api-89686018.html)页。
