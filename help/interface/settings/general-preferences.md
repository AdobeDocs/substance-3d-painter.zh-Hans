---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/interface/settings/general-preferences.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中配置常规首选项，以自定义应用程序行为和用户体验。
helpx_creative_field: ""
helpx_description: Painter > Interface > Settings > General preferences
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 常规首选项
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 2%

---


# 常规首选项

![](../../assets/settings-general_1.png)

本页说明应用程序的主要设置。

## 界面选项

![](../../assets/settings-interface.png)

| 设置 | 描述 |
| --- | --- |
| **语言** | 定义应用程序中界面使用的语言。 此设置需要重新启动应用程序才能生效。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>默认（系统语言）</strong>：从操作系统检索兼容的语言</li><li data-preserve-html="true"><strong>英语</strong></li><li data-preserve-html="true"><strong>德语</strong></li><li data-preserve-html="true"><strong>法语</strong></li><li data-preserve-html="true"><strong>日语</strong></li><li data-preserve-html="true"><strong>中文</strong>（简体）</li></ul> |
| **显示键盘帮助程序** | 如果已启用，则在按下某个键（如CTRL或SHIFT）时，会在视区的左下方显示键盘快捷键。 |
| **显示世界轴** | 如果启用，将在3D视图右下角显示世界轴。 |
| **背景颜色** | 选择用作视区的背景的颜色。 有两种颜色可用于创建渐变。 |
| **仅绘画时显示所选材质** | 如果启用，则在绘画时，只有当前选定的纹理集才会显示在3D视图中（暂时隐藏其他纹理集）。  **注意：**&#x200B;建议关闭此设置，因为快速更改视口中的可见性可能会影响[稀疏虚拟纹理](../../features/sparse-virtual-textures.md)的性能。 |
| **视区缩放** | 允许降低HDPI/Retina屏幕视口的分辨率以提高性能。可能的值：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>无</strong>：无缩放，视口以本机屏幕分辨率呈现。</li><li data-preserve-html="true"><strong>自动</strong>：将屏幕分辨率除以2（仅限HDPI屏幕）。</li></ul> |

## 图层栈叠选项

![](../../assets/settings-layerstack.png)

| 设置 | 描述 |
| --- | --- |
| **素材的默认UV 缩放** | 定义应用材质时，填充图层和图层栈叠中的填充效果的默认拼贴/重复值。 |
| **使用简化的缩略图** | 如果启用，图层栈栈将仅显示图标，而不计算缩览图。 使用图标可提高性能。 此设置不适用于使用UV磁贴工作流程的项目，因为这些项目将始终显示图标。 |

## 相机选项

![](../../assets/settings-camera.png)

| 设置 | 描述 |
| --- | --- |
| **转速** | 视区中摄像机的默认旋转速度的乘数。 |
| **缩放速度** | 视区中摄像机的默认缩放速度的倍数。“反转方向”允许根据鼠标移动来反转缩放方向。 |
| **轮速** | 鼠标滚轮缩放速度的乘数。“反转方向”允许根据车轮运动反转缩放方向。 |

## 烘焙选项

![](../../assets/settings-baking.png)

| 设置 | 描述 |
| --- | --- |
| **保存预处理的场景文件** | 如果启用，烘焙师使用的预处理高多边形网格将保存在磁盘上以供将来重复使用。 此设置允许更快地重新生成。 |
| **启用实时预览烘焙过程** | 如果启用，3D和2D视口将显示网格上正在计算的当前烘焙器纹理。 |
| **启用GPU 射线追踪** | 如果启用，烘焙师将尝试使用GPU而不是CPU执行光线追踪。 通常，该功能可以让烘焙师更快地完成工作。这只能在兼容的硬件上启用。 有关更多详细信息，请参阅[系统要求](../../getting-started/system-requirements.md)。 |

## 预览选项

![](../../assets/settings-preview.png)

| 设置 | 描述 |
| --- | --- |
| **本地缓存目录** | 定义生成资源缩略图时所在的辅助位置。当资源路径为只读路径时（例如在仅具有读取访问权限的网络路径上），此设置对于计算和存储资源缩略图很有用。 这样可避免在每次启动时重新计算缩览图，否则这些缩览图不会保存在磁盘上。 |
| **本地缓存预算(MB)** | 定义本地缓存的最大缓存大小。 |
| **材质预览着色器** | 定义用于生成货架中材料缩览图的着色器。 如果资源使用与默认着色器不同的工作流程，则此功能非常有用。 此设置需要重新启动应用程序才能生效。 |

## 临时文件

![](../../assets/settings-temp-1.png)

| 设置 | 描述 |
| --- | --- |
| **缓存目录** | 定义写入临时文件的位置。 这包括[稀疏虚拟纹理](../../features/sparse-virtual-textures.md)缓存。 此设置可以被[环境变量](../../pipeline-and-integration/configuration/environment-variables.md)覆盖。 |

## 稀疏虚拟纹理

![](../../assets/settings-sparse.png)

| 设置 | 描述 |
| --- | --- |
| **硬件支持加速** | 如果启用，应用程序将尝试对GPU使用稀疏纹理。 有关更多详细信息，请参阅[稀疏虚拟纹理](../../features/sparse-virtual-textures.md)页面。 此设置可以被[环境变量](../../pipeline-and-integration/configuration/environment-variables.md)覆盖。 |

## Iray硬件

![](../../assets/settings-iray.png)

本节列出了使用Iray渲染时可使用的所有兼容硬件。

CPU设置在所有计算机上都可用。 如果计算机具有&#x200B;**Nvidia GPU**，并且其版本与CUDA兼容，则此处也会列出该计算机。

>[!NOTE]
>
> 建议禁用CPU，只启用GPU硬件，以确保获得最佳渲染性能。 同时启用CPU和GPU可能会增加渲染时间。

## 隐私

![](../../assets/settings-privacy.png)

| 设置 | 描述 |
| --- | --- |
| **自动发送使用统计信息** | 如果启用，请匿名发送有关计算机硬件配置的信息以及其他使用情况数据。 这些数据可以帮助我们开发和改进软件。 |
