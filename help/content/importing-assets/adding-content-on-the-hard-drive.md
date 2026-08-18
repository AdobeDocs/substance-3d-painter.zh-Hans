---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/content/importing-assets/adding-content-on-the-hard-drive.html"
breadcrumb-title: ''
description: 了解如何将硬盘中的内容添加到Substance 3D Painter，以使用本地文件扩展您的资源库。
helpx_creative_field: ""
helpx_description: Painter > Content > Importing assets > Adding content on the hard drive
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 在硬盘上添加内容
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 2%

---


# 在硬盘上添加内容

通过将新内容直接放在硬盘驱动器上的正确位置，可以向您的库中添加资源。

默认情况下，会提供用户资源的默认文件夹，您可以在其中通过应用程序界面或手动将其放置在以下位置来添加新内容。 创建新预设（如画笔、工具、智能素材等）时，也会使用此默认库。有关详细信息，请参阅[预设](../../painting/presets/presets.md)文档。

## 资产要放在哪里？

以下是默认的&#x200B;**您的资源**&#x200B;库的位置，默认情况下在其中创建您自己的自定义内容：

<table data-preserve-html="true" style="width: 100.0%;"><colgroup> <col style="width: 15.0%;"/> <col style="width: 15.0%;"/> <col style="width: 70.0%;"/> </colgroup><tbody><tr><th>Platform</th><th>Version</th><th>路径</th></tr><tr><td rowspan="2"><strong>Windows</strong></td><td><strong>7.2</strong>或更高版本</td><td colspan="1">C:\Users\username\Documents\Adobe\Adobe Substance 3D Painter</td></tr><tr><td colspan="1">旧版</td><td colspan="1">C:\Users\username\Documents\Allegorithmic\Substance Painter</td></tr><tr><td rowspan="2"><strong>Mac</strong></td><td colspan="1"><strong>7.2</strong>或更高版本</td><td colspan="1">/用户/用户名/文稿/Adobe/Adobe Substance 3D Painter</td></tr><tr><td colspan="1">旧版</td><td colspan="1">/Users/用户名/Documents/Allegorithmic/Substance Painter</td></tr><tr><td rowspan="2"><strong>Linux</strong></td><td colspan="1"><strong>7.2</strong>或更高版本</td><td colspan="1">/home/username/Documents/Adobe/Adobe Substance 3D Painter</td></tr><tr><td>旧版</td><td colspan="1">/home/username/Documents/Allegorithmic/Substance Painter</td></tr></tbody></table>

>[!WARNING]
>
> 该应用程序附带的&#x200B;**入门资源**&#x200B;位于安装文件夹中，并且在每个新版本中被替换。 我们建议不要将个人内容放在此位置，因为每次更新时都会&#x200B;**清除这些内容**，甚至可能会导致读取/写入权限问题。\
> 最好使用&#x200B;**您的资源**&#x200B;位置或其他自定义位置。 有关如何添加自定义库位置的详细信息，请参阅[添加新库](../../interface/assets/adding-a-new-library.md)。

## 文件格式和用法

您可以将不同类型的文件导入到Substance 3D Painter Library。 将它们放在指定的文件夹中（如&#x200B;*阿尔法*、*色卡*、*效果*...） 会为资源分配一种使用类型，因此添加新内容时选择正确的文件夹非常重要。 请注意，如果添加自定义库位置，则会在该位置自动创建相应的文件夹。

| *文件格式* | *用法* | *文件夹* |
| --- | --- | --- |
| **SBSAR** | Substance 材质 | 资源/材质 |
| **SBSAR** | 滤镜 | 资源/效果 |
| **SBSAR** | 生成器 | 资源/生成器 |
| **PNG、TGA、JPEG等** | 纹理或Alpha | 资源/纹理&#x200B;**或**&#x200B;托架/Alpha |
| **HDR， EXR** | 环境或颜色Lut | 资源/环境&#x200B;**或**&#x200B;托架/Colorlut |
| **GLSL** | 着色器 | 资源/着色器 |
| **SPPR** | 画笔预设 | 资源/预设/画笔 |
| **SPPR** | 粒子预设 | 资源/预设/粒子 |
| **SPPR** | 材质预设 | 资源/预设/材料&#x200B;**或**&#x200B;资源/材料 |
| **SPPR** | 工具预设 | 资源/预设/工具 |
| **SPSM** | 智能材质 | 资源/智能素材 |
| **SPMSK** | 智能蒙版 | 资源/Smart-masks |
| **SPEXP** | 导出预设 | 托架/导出 — 预设 |

>[!NOTE]
>
> 从版本7.2.0开始，可以在库中使用自定义文件夹和类别。 可以通过[按路径筛选](../../interface/assets/filter-by-path.md)或[痕迹导航](https://helpx.adobe.com/substance-3d/unlisted/documentation/spdoc/navigating-in-the-shelf-147095659.html)在“资源”窗口中访问它们。

>[!WARNING]
>
> 无法直接使用&#x200B;**SBS**（不是SBSAR）文件，需要从Substance 3D Designer中将它们导出为SBSAR。
