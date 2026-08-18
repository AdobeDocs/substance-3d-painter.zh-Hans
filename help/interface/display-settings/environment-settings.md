---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/interface/display-settings/environment-settings.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中配置环境设置，以控制材质预览的光照和背景。
helpx_creative_field: ""
helpx_description: Painter > Interface > Display settings > Environment settings
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 环境设置
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 0%

---


# 环境设置

**显示设置**&#x200B;的此部分控制视区中的光照。

## 环境

![](../../assets/env-settings.png)

| *设置* | *描述* |
| --- | --- |
| **环境映射** | 用于照亮场景的环境映射纹理。 可以使用“环境”预设在[资源](../assets/assets.md)窗口中找到。单击按钮以打开一个迷你架并选择其他环境图。 |
| **覆盖环境映射色彩空间** | 如果当前项目使用[色彩管理](../../features/color-management/color-management.md)，则可以启用此设置以覆盖环境映射的色彩空间。 |
| **环境不透明度** | 控制视区背景中环境纹理的可见性/不透明度。 此设置不影响场景的光照。 |
| **环境曝光** | 曝光值(EV)是表示固定场景明亮度的数字。 此设置允许偏移默认明亮度值。在使用随应用程序提供的环境映射时，此设置应保持为0。 使用不正确的曝光值为资源添加纹理可能会导致其他应用程序出现颜色校准问题。 |
| **环境轮换** | 控制环境纹理的水平旋转。 用于旋转场景中的光照并更改对象的反应方式。 可以使用[快捷键](../settings/shortcuts.md)控制。 |
| **环境模糊** | 控制视区的背景中环境纹理将呈现的清晰或模糊程度。 此设置对光照没有影响。 |
| **环境对齐方式** | 控制环境纹理如何在视区内绕3D模式旋转。 当设置为局部时，此设置可用于照亮3D模型下的区域。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>世界</strong>（默认）：环境与场景对齐，并绕3D模型的上轴旋转。</li><li data-preserve-html="true"><strong>局部</strong>：环境与相机对齐，并围绕相机的上轴旋转。</li></ul> |

## 阴影

![](../../assets/shadow-2.png)

| *设置* | *描述* |
| --- | --- |
| **阴影** | 启用/禁用视口中阴影的渲染。 |
| **计算模式** | 控制计算阴影的速度。<ul data-preserve-html="true"><li data-preserve-html="true"><strong>密集型</strong> ：计算速度快，但可以冻结视区的渲染。</li><li data-preserve-html="true"><strong>平均</strong> ：密集模式和轻量模式的平均值。</li><li data-preserve-html="true"><strong>轻量级</strong> ：（默认）计算使阴影慢了几秒，但不会降低视口性能。</li></ul> |
| **阴影不透明度** | 控制场景中可见的阴影量。 |
