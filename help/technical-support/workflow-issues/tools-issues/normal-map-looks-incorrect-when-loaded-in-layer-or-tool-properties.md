---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/workflow-issues/tools-issues/normal-map-looks-incorrect-when-loaded-in-layer-or-tool-properties.html"
breadcrumb-title: ''
description: 了解如何修复Substance 3D Painter图层和工具属性中的法线映射显示问题，以获取准确的表面细节。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Workflow Issues > Tools Issues > Normal map looks incorrect when loaded in layer or tool properties
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 在图层或工具属性中加载法线图时，法线图看起来不正确
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---


# 在图层或工具属性中加载法线图时，法线图看起来不正确

将法线加载到填充图层的当前工具时，如果这是OpenGL法线图，则此项可能会显示不正确。\
原因很简单：Substance 3D Painter引擎假设加载的法线映射在默认情况下是DirectX的。

通过单击Substance素材或专用通道旁边的小箭头，可以轻松编辑此行为：

![](../../../assets/channel-format-override.png)
