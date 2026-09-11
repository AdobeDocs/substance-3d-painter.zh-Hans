---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/technical-issues/rendering-issues/mesh-appears-pink-in-the-viewport.html"
breadcrumb-title: ''
description: 了解如何在视口中修复粉红色网格外观，以恢复正确的材料渲染。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > Rendering Issues > Mesh appears pink in the viewport
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 网格在视口中显示为粉红色
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---


# 网格在视口中显示为粉红色

![](../../../assets/pink-mesh.jpg){width="400px"}

网格在视口中可能显示&#x200B;**粉红色**，因为用于绘制它的&#x200B;**着色器** **不再编译**（如&#x200B;**日志窗口**&#x200B;中所述）。 这可能是由于过时的着色器不支持最新版本的着色器 API所致。

修复方法如下：

* 对于&#x200B;**默认着色器**：按照[更新着色器](../../../interface/shader-settings/updating-a-shader.md)页中的分步过程操作。
* 对于&#x200B;**自定义着色器**：查看log窗口以及[着色器 API](https://helpx.adobe.com/substance-3d/unlisted/documentation/spdoc/custom-shader-api-89686018.html)页中的错误消息。
