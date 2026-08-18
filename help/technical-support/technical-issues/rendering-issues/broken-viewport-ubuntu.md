---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/technical-support/technical-issues/rendering-issues/broken-viewport-ubuntu.html"
breadcrumb-title: ''
description: 了解如何修复Substance 3D Painter中Ubuntu上的视口中断或无响应的问题，以便进行正确的3D渲染。
helpx_creative_field: ""
helpx_description: Viewport appears broken or unresponsive on Ubuntu
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 在Ubuntu上，视口显示为已损坏或无响应
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---


# 在Ubuntu上，视口显示为已损坏或无响应

从版本11.1开始在Ubuntu上从Steam运行Painter时，视口可能会损坏或无响应。

这与Painter未从为其分配正确的GPU开始有关。 在Ubuntu上，集成的GPU而不是单独的GPU可能最终被选中。 Painter通过Steam继承此配置，这可能会造成问题。

目前存在几种解决方案：

1. 从终端发蒸气。 这将强制执行不同的上下文，并且应使Steam和Painter在正确的GPU上运行。
1. 编辑Steam快捷键以禁用<b>使用专用图形卡</b>运行。 然后照常运行Steam。

有关详细信息，请参阅[此Github问题](https://github.com/ValveSoftware/steam-for-linux/issues/9940)。
