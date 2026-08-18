---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/features/color-management/color-management-with-opencolorio.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中使用OpenColorIO色彩管理实现跨管道的一致颜色工作流。
helpx_creative_field: ""
helpx_description: Painter > Features > Color management > Color management with OpenColorIO
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 使用OpenColorIO进行色彩管理
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '675'
ht-degree: 8%

---


# 使用OpenColorIO进行色彩管理

此页面列出了与OpenColorIO (OCIO)相关的色彩管理设置。

## Project settings

![](../../assets/project-settings-3.png)

通过[新建项目](../../getting-started/project-creation.md)窗口或使用[项目配置](../../interface/project-configuration.md)窗口创建新项目时，可以设置项目设置。

>[!NOTE]
>
> 如果存在&#x200B;**OCIO**&#x200B;环境变量并指定了有效的配置文件，它将覆盖并禁用UI中的设置。

可用设置包括：

<table data-preserve-html="true" style="width: 99.9039%;"><colgroup><col style="width: 12.512%;"/><col style="width: 21.1742%;"/><col style="width: 66.3122%;"/></colgroup><tbody><tr><th style="width: 12.5%;">章节</th><th style="width: 21.1538%;">设置</th><th style="width: 66.25%;">描述</th></tr><tr><td rowspan="3" style="width: 12.5%;"><strong>配置</strong></td><td style="width: 21.1538%;"><strong>色彩管理</strong></td><td style="width: 66.25%;"><p>定义用于管理颜色的引擎。</p><p>可能的值：</p><ul><li><strong>旧版</strong>（默认）：使用预定义的sRGB/线性sRGB灰度系数颜色校正。</li><li><strong>OpenColorIO</strong>：使用OCIO集成。</li><li><strong>Adobe的ACE</strong>：Adobe 颜色引擎，用于支持ICC配置文件。</li></ul></td></tr><tr><td style="width: 21.1538%;"><strong>OpenColorIO 配置</strong></td><td style="width: 66.25%;"><p>用于驱动色彩管理设置的配置文件。</p><p>可能的值：</p><ul><li><strong>Substance</strong>（默认）：使用线性灰度系数作为工作空间。</li><li><strong>ACES 1.0.3</strong>：使用ACEScg作为工作空间。</li><li><strong>ACES 1.2</strong>：使用ACEScg作为工作空间。</li><li><strong>自定义</strong>：使用自定义配置文件。</li></ul></td></tr><tr><td style="width: 21.1538%;"><strong>配置文件</strong></td><td style="width: 66.25%;">OCIO配置文件的路径。 如果配置模式未设置为<strong>自定义</strong>，则禁用。</td></tr><tr><th style="width: 12.5%;"><br/></th><th style="width: 21.1538%;"><br/></th><th style="width: 66.25%;"><br/></th></tr><tr><td rowspan="2" style="width: 12.5%;"><strong>颜色设置</strong></td><td style="width: 21.1538%;"><strong>工作色彩空间</strong></td><td style="width: 66.25%;">引擎在应用程序内部工作所用的色彩空间。 这是颜色空间，纹理可以从该空间转换为（导入）或从（导出）。</td></tr><tr><td colspan="1"><strong>标准 sRGB 色彩空间</strong></td><td colspan="1"><p>与[标准sRGB](https://en.wikipedia.org/wiki/SRGB)色彩空间匹配的色彩空间(IEC 61966-2-1:1999)。</p><p>此色彩空间在应用程序内的多个位置使用：</p><ul><li>转换拾色器十六进制字段中的颜色集。</li><li>在拾色器中保存和载入色板。</li><li>在拾色器列表中作为显示列出。</li></ul></td></tr><tr><th style="width: 12.5%;"><br/></th><th style="width: 21.1538%;"><br/></th><th style="width: 66.25%;"><br/></th></tr><tr><td rowspan="4" style="width: 12.5%;"><strong>位图导入色彩空间默认</strong></td><td style="width: 21.1538%;"><strong>8 位图像</strong></td><td style="width: 66.25%;">导入8位图像文件时默认使用的色彩空间。</td></tr><tr><td style="width: 21.1538%;"><strong>16 位图像</strong></td><td style="width: 66.25%;">导入16位图像文件时默认使用的色彩空间。</td></tr><tr><td style="width: 21.1538%;"><strong>浮点图像</strong></td><td style="width: 66.25%;">导入HDR/EXR图像文件时默认使用的色彩空间。</td></tr><tr><td style="width: 21.1538%;"><strong>自动检测色彩空间</strong></td><td style="width: 66.25%;"><p>允许根据特定设置从资源定义色彩空间。</p><p>可能的值：</p><ul><li><strong>已禁用</strong>：使用默认颜色设置，忽略资源配置。</li><li><strong>解析文件名</strong>（默认）：使用OCIO [命名约定](https://opencolorio.readthedocs.io/en/latest/guides/authoring/rules.html?highlight=filename#strictparsing)提取资源使用的色彩空间名称。</li><li><strong>使用配置文件规则</strong>：使用OCIO配置确定如何分配色彩空间。 此参数的优先级高于以前的图像文件色彩空间设置。</li></ul></td></tr><tr><th style="width: 12.5%;"><br/></th><th style="width: 21.1538%;"><br/></th><th style="width: 66.25%;"><br/></th></tr><tr><td style="width: 12.5%;"><strong>Substance材料</strong></td><td style="width: 21.1538%;"><strong>材质色彩空间默认</strong></td><td style="width: 66.25%;"><p>定义用于Substance素材的色彩空间受色彩管理的输入/输出（通道列表请参阅下文）。</p></td></tr><tr><th style="width: 12.5%;"><br/></th><th style="width: 21.1538%;"><br/></th><th style="width: 66.25%;"><br/></th></tr><tr><td rowspan="3" style="width: 12.5%;"><strong>导出色彩空间</strong><br/><br/><br/></td><td style="width: 21.1538%;"><strong>8 位图像</strong></td><td style="width: 66.25%;">导出8位图像文件时默认使用的色彩空间。</td></tr><tr><td style="width: 21.1538%;"><strong>16 位图像</strong></td><td style="width: 66.25%;">导出16位图像文件时默认使用的色彩空间。</td></tr><tr><td style="width: 21.1538%;"><strong>浮点图像</strong></td><td style="width: 66.25%;">导出HDR/EXR图像文件时默认使用的色彩空间。</td></tr></tbody></table>

### OpenColorIO角色

支持以下角色，并允许更改色彩空间的默认选择：

| 角色名称 | 描述 |
| --- | --- |
| **substance\_3d\_painter\_standard\_srgb** | 用于指定与[标准sRGB](https://en.wikipedia.org/wiki/SRGB) (IEC 61966-2-1:1999)匹配的色彩空间的角色。 |
| **substance\_3d\_painter\_bitmap\_import\_8bit** | 用于指定用于导入8位图像的色彩空间的角色。 |
| **substance\_3d\_painter\_bitmap\_import\_16bit** | 用于指定用于导入16位图像的色彩空间的角色。 |
| **substance\_3d\_painter\_bitmap\_import\_floating** | 用于指定用于导入HDR图像的色彩空间的角色。 |
| **substance\_3d\_painter\_substance\_material** | 用于指定色彩素材中用于色彩管理通道的Substance空间的角色。 |
| **substance\_3d\_painter\_bitmap\_export\_8bit** | 用于指定导出8位纹理时使用的色彩空间的角色。 |
| **substance\_3d\_painter\_bitmap\_export\_16bit** | 用于指定导出16位纹理时使用的色彩空间的角色。 |
| **substance\_3d\_painter\_bitmap\_export\_floating** | 用于指定导出HDR纹理时使用的色彩空间的角色。 |

>[!NOTE]
>
> 应用程序附带的OCIO配置可用作有关如何使用这些特定角色的示例。
