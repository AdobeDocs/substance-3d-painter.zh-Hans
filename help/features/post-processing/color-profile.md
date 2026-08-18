---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/features/post-processing/color-profile.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中使用颜色配置文件后期处理功能来应用颜色分级和LUT变换。
helpx_creative_field: ""
helpx_description: Painter > Features > Post Processing > Color Profile
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 颜色配置文件
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 0%

---


# 颜色配置文件

![](../../assets/doc-lut-example.jpg){width="700px"}

Substance 3D Painter允许通过加载&#x200B;**LUT**&#x200B;纹理来将&#x200B;**颜色配置文件**&#x200B;分配给&#x200B;**视口**。\
颜色配置文件可用于校准屏幕的最终颜色以匹配目标，例如特定相机。 通常，配置文件会通过更改亮度、灰度系数、对比度甚至色彩平衡来操纵颜色。

>[!NOTE]
>
> **LUT**&#x200B;表示“**查找表**”。 这是一种将颜色分级作为后期效果执行的最优化方法。 LUT用于弥补源和结果之间的差异。\
>  Substance 3D Painter使用存储为任何可能分辨率的&#x200B;**2D纹理**（浮动）的&#x200B;**3D** LUT（默认为&#x200B;**2048x128像素**）。 这意味着存储颜色操作的立方体被分成多个片并排显示。 有关更多技术详细信息，请参阅&#x200B;**GPU Gem**&#x200B;文章： <http://http.developer.nvidia.com/GPUGems2/gpugems2_chapter24.html>

## 使用颜色配置文件

可通过“显示设置”窗口载入颜色配置文件。\
选中“**激活颜色配置文件**”复选框以影响视区并启用颜色配置文件。

![](../../assets/color-profile-ui.png)

* 当“激活颜色配置文件”为&#x200B;**禁用**&#x200B;时，将以&#x200B;**sRGB**&#x200B;为材质视图渲染视区（对于某些特定通道，为线性）
* 当“激活颜色配置文件”为&#x200B;**已启用**&#x200B;时，视区的渲染将在每个视图（包括独奏通道）的&#x200B;**线性/Raw**&#x200B;中完成

如果LUT纹理加载到资源插槽中，则它将用于在&#x200B;**材质模式**&#x200B;下处理视区的渲染。\
否则，渲染将显示为线性/原始数据（例如，带有单独通道视图）。

**白场**&#x200B;设置可用于更改输入图像的色调映射（在LUT生效之前）。\
例如，如果查看太阳，该值应大于1（缺省值）。 为了获得理想的曝光度，必须将白场设置为图像的高值区域。

白场公式如下：

```
float Value = 1.0f / WhitePoint; // Value from the user interface 

float3 Output = clamp( HDR.rgb * Value, 0.0f, 1.0f );
```


可以在使用颜色配置文件之前应用特定的色调映射。 查看[色调映射](tone-mapping.md)中可用的功能。\
Substance 3D Painter不处理输入颜色，而是通过白场设置处理。 例如，没有应用Shaper LUT。

## 创建颜色配置文件

启用“**激活颜色配置文件**”后，Substance 3D Painter会将视区转换为&#x200B;**线性**&#x200B;渲染。 这意味着在应用LUT时，需要将颜色从线性配置文件转换为所需的目标。

### 方法1 ：修改身份LUT

可在支持<b>32位浮动</b>纹理的软件（如<b>Substance 3D Designer</b>）中编辑标识LUT。 下载身份LUT作为制作新配置文件的起点：

[下载color\_profile\_linear.exr](https://github.com/AdobeDocs/painter-python-api/raw/refs/heads/main/static/misc/color_profile_linear.exr)

### 方法2 ：使用OpenColor IO生成LUT纹理

安装&#x200B;**OpenColor IO**&#x200B;工具。 然后，下载示例OCIO配置，可从此处获得： <http://opencolorio.org/downloads.html>\
从该处运行具有以下参数的&#x200B;**ociolutimage**&#x200B;程序：

```
ociolutimage --generate --cubesize 64 --config nuke-default/config.ocio --colorconvert linear srgb --output lutLinearToSRGB.exr
```


**注意**：也可以使用&#x200B;**ocioconvert**&#x200B;程序对此LUT应用颜色转换，从而使用&#x200B;**OpenColor IO**&#x200B;修改标识LUT。

### 导入新的颜色配置文件

只需打开导入窗口（或将LUT拖放到货架中）。 在Substance 3D Painter中导入LUT纹理时，请确保将“**colorlut**”**用法**&#x200B;分配给新资源。 否则，资源将无法正确显示在盘架中。

有关详细信息，请参阅有关导入新资源的文档： [通过导入窗口添加资源](https://helpx.adobe.com/cn/substance-3d/unlisted/documentation/spdoc/adding-content-via-the-import-window-151584824.html)
