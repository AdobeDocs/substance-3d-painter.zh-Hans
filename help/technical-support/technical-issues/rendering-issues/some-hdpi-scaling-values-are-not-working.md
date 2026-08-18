---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/technical-support/technical-issues/rendering-issues/some-hdpi-scaling-values-are-not-working.html"
breadcrumb-title: ''
description: 了解如何修复Substance 3D Painter中的HDPI缩放值问题，以便获得正确的高分辨率显示支持。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > Rendering Issues > Some HDPI scaling values are not working
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 某些HDPI缩放值不起作用
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---


# 某些HDPI缩放值不起作用

在Windows上，某些HDPI缩放值（用于在高分辨率显示器上缩放界面）可能无法正常工作。\
这是因为我们的窗口框架(Qt)不支持它们。 在实际上由框架本身的提供商进行管理之前，我们无法修复此问题。

因此，根据您的设置，您可能会遇到以下行为：

* 120 DPI （**125%**&#x200B;缩放） — 渲染为96 DPI （**100%**&#x200B;缩放）
* 144 DPI （**150%**&#x200B;缩放） — 渲染为192 DPI （**200%**&#x200B;缩放）
* 168 DPI （**175%**&#x200B;缩放） — 渲染为192 DPI （**200%**&#x200B;缩放）

有关详细信息，请参阅： <https://bugreports.qt.io/browse/QTBUG-55654>
