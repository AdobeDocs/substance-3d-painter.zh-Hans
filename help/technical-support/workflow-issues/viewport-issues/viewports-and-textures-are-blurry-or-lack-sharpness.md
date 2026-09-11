---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/workflow-issues/viewport-issues/viewports-and-textures-are-blurry-or-lack-sharpness.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中修复模糊的视口和纹理，以确保清晰、锐利的视觉品质。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Workflow Issues > Viewport Issues > Viewports and textures are blurry or lack sharpness
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 视区和纹理模糊或缺乏锐度
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 1%

---


# 视区和纹理模糊或缺乏锐度

视口可能由于各种原因而显得模糊。

## 高DPI屏幕(Retina)设置

默认情况下，Substance 3D Painter会缩小高DPI/Retina屏幕上的视口分辨率以改善性能。

可通过更改&#x200B;**视口缩放**&#x200B;参数，在[主要设置](https://helpx.adobe.com/substance-3d/unlisted/documentation/spdoc/general-71008262.html)中更改此行为。

## Texture filtering

视口使用mipmaps和纹理筛选来流入/流出[Sparse Virtual Texture](../../../features/sparse-virtual-textures.md)以提高性能。 在某些情况下，这会导致模糊纹理。

可以通过[纹理设置](../../../interface/display-settings/viewport-settings.md)参数下的“显示设置”窗口调整视口筛选。
