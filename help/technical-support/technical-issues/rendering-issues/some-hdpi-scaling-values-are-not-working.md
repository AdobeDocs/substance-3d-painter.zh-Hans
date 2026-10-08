---
breadcrumb-title: ""
description: 了解如何修复Substance 3D Painter中的HDPI缩放值问题，以便获得正确的高分辨率显示支持。
title: 某些HDPI缩放值不起作用
user-guide-description: ""
user-guide-title: ""
source-git-commit: 6b6d52207ca1d043aaa1b2b14145b6b49d4c1942
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
