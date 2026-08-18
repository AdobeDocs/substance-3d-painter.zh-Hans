---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/features/color-management/color-management-with-adobe-ace-icc.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中使用AdobeACE和ICC色彩管理实现一致的色彩工作流程。
helpx_creative_field: ""
helpx_description: Painter > Features > Color management > Color management with Adobe ACE - ICC
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 使用AdobeACE - ICC进行色彩管理
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---


# 使用AdobeACE - ICC进行色彩管理

本页列出了与ICC配置文件使用图像的Adobe 颜色引擎(ACE)相关的色彩管理设置。

## Project settings

![](../../assets/cm-ace.png)

通过[新建项目](../../getting-started/project-creation.md)窗口或使用[项目配置](../../interface/project-configuration.md)窗口创建新项目时，可以设置项目设置。

>[!NOTE]
>
> 如果加载了环境变量（请参阅下文）或预设文件，则UI中的设置将被禁用。

可用设置包括：

| 章节 | 设置 | 描述 |
| --- | --- | --- |
| **配置** | **色彩管理** | 定义用于管理颜色的引擎。可能的值：<ul data-preserve-html="true"> <li data-preserve-html="true"><strong>旧版</strong>（默认）：使用预定义的sRGB/线性sRGB灰度系数颜色校正。</li> <li data-preserve-html="true"><strong>OpenColorIO</strong>：使用OCIO集成。</li> <li data-preserve-html="true"><strong>Adobe的ACE</strong>：Adobe 颜色引擎，用于支持ICC配置文件。</li> </ul> |
|  | **使用预设文件** | 如果启用，请允许通过json配置文件删除色彩管理设置。 |
|  | **预设文件** | 预设文件的路径（json格式）。 有关更多详细信息，请参阅下文。 |
|  |  |  |
| **颜色设置** | **工作色彩空间** | 引擎在应用程序内部工作所用的色彩空间。 纹理可以从该色彩空间转换为（导入）或从（导出）。可能的值有：<ul data-preserve-html="true"> <li data-preserve-html="true"><strong>线性sRGB IEC61966-2.1</strong>（默认）</li> <li data-preserve-html="true"><strong>ACEScg ACES工作空间AMPAS S-2014-004</strong></li> <li data-preserve-html="true"><strong>线性Adobe RGB (1998)</strong></li> </ul> |
|  | **渲染方法** | 指定用于在色彩空间之间转换颜色的方法。可能的值：<ul data-preserve-html="true"> <li data-preserve-html="true"><strong>可感知</strong></li> <li data-preserve-html="true"><strong>饱和度</strong>（默认）</li> <li data-preserve-html="true"><strong>相对色度</strong></li> <li data-preserve-html="true"><strong>绝对色度</strong></li> </ul> |
|  |  |  |
| **位图导入色彩空间默认值** | **8位图像** | 导入8位图像文件时默认使用的色彩空间。 |
|  | **16位图像** | 导入16位图像文件时默认使用的色彩空间。 |
|  | **浮点图像** | 导入HDR/EXR图像文件时默认使用的色彩空间。 |
|  | **可用时使用嵌入的ICC配置文件（推荐）** | 如果启用，请使用ICC配置文件（自图像文件开始）来调整其颜色。 |
|  |  |  |
| **Substance的材质** | **素材色彩空间默认值** | 定义对Substance素材使用哪种色彩空间进行色彩管理的输入/输出。 |
|  |  |  |
| **导出色彩空间** | **8位图像** | 导出8位图像文件时默认使用的色彩空间。 |
|  | **16位图像** | 导出16位图像文件时默认使用的色彩空间。 |
|  | **浮点图像** | 导出HDR/EXR图像文件时默认使用的色彩空间。 |

## 使用预设文件

![](../../assets/cm-ace-env-var.png)

创建新项目时可以使用预设文件（json格式）来驱动ACE设置。

### 环境变量

环境变量&#x200B;**PAINTER\_ACE\_CONFIG**&#x200B;可用于指定预设文件的路径。 如果存在，应用程序将始终使用预设文件来驱动色彩管理设置。 将在界面中禁用这些设置。

有关更多详细信息，请参阅[环境变量](../../pipeline-and-integration/configuration/environment-variables.md)页面。

### 预设示例

以下是可以用作预设文件的json文件示例：

```
{ 

  "color settings": { 

    "working color space": "Linear Adobe RGB (1998)", 

    "rendering intent": "Saturation" 

  }, 

  "bitmap import color space defaults" : { 

    "8 bit images": "image P3", 

    "16 bit images": "image P3", 

    "floating point images": "Raw", 

    "use embedded ICC profiles when available": false 

  }, 

  "substance material": { 

    "material color space default": "image P3" 

  }, 

  "export colors spaces" : { 

    "8 bit images": "image P3", 

    "16 bit images": "image P3", 

    "floating point images": "Raw" 

  } 

} 
```
