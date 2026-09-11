---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/technical-support/workflow-issues/viewport-issues/mesh-faces-disappear-when-looking-at-them-from-behind.html"
breadcrumb-title: ''
description: 了解如何修复在视口中从后方观看时网格脸部消失的问题，以确保网格正确可见。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Workflow Issues > Viewport Issues > Mesh faces disappear when looking at them from behind
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 从后面查看脸部时，这些颜色消失
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---


# 从后面查看脸部时，这些颜色消失

默认情况下，视口中的网格可能不会显示网格多边形的背面（背面）。 这是因为它们被当前着色器所淘汰。

要显示脸部的背面，只需在[着色器设置](../../../interface/shader-settings/shader-settings.md)中将当前着色器更改为&#x200B;**pbr-metal-rough-alpha-test**。
