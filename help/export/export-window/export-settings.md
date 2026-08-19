---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/getting-started/export/export-window/export-settings.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中配置导出设置，以控制纹理分辨率、格式和输出选项。
helpx_creative_field: ""
helpx_description: Painter > Getting Started > Export > Export window > Export settings
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 导出设置
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '958'
ht-degree: 1%

---


# 导出设置

![](../../assets/image2023-1-30-13-22-30.png){width="500px"}

<b>导出纹理窗口</b>的<b>导出设置选项卡</b>允许您配置导出纹理的合成、大小和位置。

## 常规和纹理集配置

![](../../assets/texture-set-list-1.png)

窗口的第一个元素是左侧的“纹理集”列表。 使用“全局设置”部分可访问所有纹理集的通用参数。 这样可以轻松调整单个设置集以应用于项目的所有纹理集。 对单个纹理集设置所做的更改将覆盖该纹理集的全局设置。 例如，如果将“全局设置”中的分辨率设置为2048，并将1024设置为特定“纹理集”的覆盖，则将导致以2048分辨率导出所有纹理集（设置为1024的纹理集除外）。

每个纹理集名称旁的复选框指示是否将导出关联的纹理。

下拉菜单适用于包含大量纹理集的项目，因为它允许您通过<b>全部选中</b>、<b>全部取消选中</b>和<b>反转所有</b>操作来快速修改选区。

## 常规导出参数

![](../../assets/image2023-1-30-13-23-7.png)

本节包含将生成的每个纹理的共享设置：

| 设置 | 描述 |
| --- | --- |
| <b>输出目录</b> | 导出纹理的存储位置。 |
| <b>输出模板</b> | 选择用于将通道命名并合成到纹理文件中的输出模板。 有关模板的更多信息，请参阅[输出模板](../export-presets/export-presets.md)列表。 |
| <b>文件类型</b> | 文件格式及其位深度。 如果选择选项<b>基于输出模板</b>，将从导出预设继承文件格式（允许按纹理而不是全局确定格式和位深度）。 可用的位深度取决于文件类型；有关详细信息，请参阅下表。 |
| <b>大小</b> | 导出的纹理文件的分辨率。 可能的值：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>基于每个纹理集的大小</b></li> <li data-preserve-html="true"><b>128</b></li> <li data-preserve-html="true"><b>256</b></li> <li data-preserve-html="true"><b>512</b></li> <li data-preserve-html="true"><b>1024</b></li> <li data-preserve-html="true"><b>2048</b></li> <li data-preserve-html="true"><b>4096</b></li> <li data-preserve-html="true"><b>8192</b>（仅适用于具有超过1.5 GB Vram的GPU）</li> </ul> |
| <b>正在填充</b> | 如何填充UV 岛以外的区域到纹理内部。 可能的值为：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>无填充（穿透）</b>：按原样使用纹理的当前状态。</li> <li data-preserve-html="true"><b>无限扩展</b>：拉伸UV 岛边框，直到它们达到相邻边框或纹理末尾。</li> <li data-preserve-html="true"><b>扩展+透明</b>：将UV 岛边框拉伸到给定的距离（以像素为单位），其余部分为透明。</li> <li data-preserve-html="true"><b>扩展+默认背景色</b>：将UV 岛边框拉伸到给定距离（以像素为单位），其余部分使用纹理集通道的默认颜色填充。</li> <li data-preserve-html="true"><b>扩展+默认背景色</b>：将UV 岛边框拉伸到给定距离（以像素为单位），其余部分使用纹理集通道的默认颜色填充。</li> <li data-preserve-html="true"><b>扩展+扩散</b>：将UV 岛边框拉伸到给定的距离（以像素为单位），其余部分填充模糊版本的UV 岛（基于mip映射）。</li> </ul> |

>[!NOTE]
>
> **psd**&#x200B;文件格式是一个容器，这意味着输出映射将汇集到磁盘上的单个文件中。

### 抖动

导出8位纹理会导致渐变中出现条纹。 这对于正常映射和Height映射尤其明显。 解决该问题的方法有两种：使用较高的精度或采用抖动补偿。

精度更高（16位或32位）是理想选择，但可能无法与所有应用程序兼容。 最值得注意的是，游戏引擎通常压缩到8位。 抖动会引入噪声，有助于在仍然使用8位信息的同时缓解带状问题。

![](../../assets/dither-1.jpg)

### 纹理文件格式

以下是Painter支持的所有导出文件格式列表：

| 格式名称 | 格式扩展 | 支持的位深度 |
| --- | --- | --- |
| **位图** | bmp | 8， 8 +抖动 |
| **OpenEXR** | exr | 16（浮动），32（浮动） |
| **图形交换格式** | gif | 8， 8 +抖动 |
| **Radiance HDR** | hdr | 32（浮动） |
| **图标** | ico | 8， 8 +抖动 |
| **Jpeg 2000** | j2k | 8， 8 +抖动， 16 |
| **Jpeg网络图形** | jng | 8， 8 +抖动， 16 |
| **Jpeg 2000** | jp2 | 8， 8 +抖动， 16 |
| **Jpeg** | jpeg | 8， 8 +抖动 |
| **JPEG扩展范围** | jpeg-xr | 8， 8 +抖动， 16， 32（浮动） |
| **便携位图** | pbm | 8， 8 +抖动， 16 |
| **便携浮点图** | pfm | 32（浮动） |
| **便携灰度图** | pgm | 8， 8 +抖动， 16 |
| **便携网络图形** | png | 8， 8 +抖动， 16 |
| **便携像素地图** | ppm | 8， 8 +抖动， 16 |
| **Photoshop文档** | psd | 8， 8 +抖动， 16 |
| **Truevision TGA** | targa | 8， 8 +抖动 |
| **标记图像文件格式** | tiff | 8， 8 +抖动， 16， 32（浮动） |
| **无线应用协议位图格式** | wbmp | 8， 8 +抖动 |
| **WebP** | webp | 8， 8 +抖动 |
| **X PixMap** | xpm | 8， 8 +抖动 |

## Output maps

选择特定纹理集后，输出映射部分对该纹理集可见。

![](../../assets/export-output-maps.png)

此部分列出了将根据当前导出预设生成的所有纹理。 如果启用了[色彩管理](../../features/color-management/color-management.md)，则还将显示纹理名称模板、文件格式和位深度以及色彩空间。

此部分允许您禁用特定文件的导出或覆盖<b>文件位深度</b>和<b>格式</b>。

![](../../assets/export-override.gif)

## 导出 USD 资源

选中此框将允许您以USD格式导出。 与<b>输出模板</b>中可用的USDz (Apple AR)预设不同，此导出将考虑您为导出配置的任何模板或参数。 选中“USD资源”框时，将导出以下文件 — 

* 带有纹理映射的文件夹
* 指向纹理映射文件夹的&#x200B;*.usda*。
* 一个可选的.usd，用于将材质与原始网格文件组合在一起。 它可以直接用于Omniverse，以显示自动应用了素材的网格。
* 可选的.usd文件，其中包括项目中使用的网格。 仅当原始网格文件不是USD或者Painter的自动展开功能用于生成UV时，才会导出该文件。
