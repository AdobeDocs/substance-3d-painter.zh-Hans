---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/getting-started/export/export-window/output-templates.html"
breadcrumb-title: ''
description: 了解如何使用Substance 3D Painter导出窗口中的输出模板来配置纹理导出格式和命名。
helpx_creative_field: ""
helpx_description: Painter > Getting Started > Export > Export window > Output templates
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 输出模板
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '748'
ht-degree: 1%

---


# 输出模板

![](../../assets/export-output-template.png){width="500px"}

“输出模板”选项卡允许您管理和创建新输出模板。 您可以使用输出模板来修改导出纹理的名称、格式和配置。

## 预设列表

![](../../assets/export-preset-list.png)

预设列表会显示所有可用的输出模板。 此列表包含[默认输出模板](../export-presets/default-presets.md)的集合，以及您创建的所有自定义模板。

在此列表中，模板可以<b>创建</b>、<b>重命名</b>、<b>重复、</b>或<b>删除</b>。

| 操作 | 视觉 | 描述 |
| --- | --- | --- |
| **重复** | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c1_image" src="../../assets/preset-duplicate.png"/></div> | 创建列表中当前所选输出模板的副本。 |
| **删除** | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r2-column-c1_image" src="../../assets/preset-remove.png"/></div> | 删除列表中当前选定的输出模板。  **注意：**&#x200B;删除模板的操作无法撤消。 |
| **添加** | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r3-column-c1_image" src="../../assets/preset-add.png"/></div> | 添加新的空输出模板。 |
| **双击** | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r4-column-c1_image" src="../../assets/rename-preset.gif"/></div> | 重命名所选输出模板。 |
| **右键单击** | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r5-column-c1_image" src="../../assets/right-click.gif"/></div> | 右键单击模板以打开上下文菜单，您可以在其中删除、重命名或复制模板。 |

## 输出映射列表

![](../../assets/export-preset-config.png)

此部分列出模板及其合成将生成的所有纹理。

### 映射类型和关键字

顶行列出了所有可创建的纹理类型：

| 按钮 | 视觉 | 描述 |
| --- | --- | --- |
| **灰色** | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r1-column-c1_image" src="../../assets/export-type-gray.png"/></div> | 添加新的灰度地图。 |
| **RGB** | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r2-column-c1_image" src="../../assets/export-type-rgb.png"/></div> | 添加新的RGB色图。 |
| **R+G+B** | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r3-column-c1_image" src="../../assets/export-type-r-g-b.png"/></div> | 添加具有3个单独灰度插槽的新RGB图。 |
| **RGB+A** | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r4-column-c1_image" src="../../assets/export-type-rgb-a.png"/></div> | 添加一个新的RGB映射以及一个Alpha（灰度）插槽。 |
| **R+G+B+A** | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table1_row-r5-column-c1_image" src="../../assets/export-type-r-g-b-a.png"/></div> | 添加具有4个单独的灰度插槽的新RGBA映射。 |

>[!NOTE]
>
> 某些类型为空或共享同一输入图时可以合并/折叠：
> 
> ![](../../assets/split-collapse.gif)

### 映射名称

![](../../assets/outputmap-name.png)

每个纹理都可以使用自定义命名约定进行命名。 可以添加一些关键字（借助&#x200B;**$**&#x200B;按钮），以便在生成最终文件时自动替换为应用程序：

| 关键字 | 描述 |
| --- | --- |
| **$项目** | 替换为项目文件的名称(.spp)。 |
| **$网格** | 替换为网格文件的名称（输入网格文件，如.fbx） |
| **$textureset** | 替换为从中生成纹理的材质/纹理集的名称。 |
| **$udim** | 替换为从中生成纹理的UDIM号。 |
| **$色彩空间** | 替换为给定通道所用的色彩空间名称（RGB或G，忽略Alpha）。 |

### 映射文件格式和位深度

![](../../assets/outputmap-file-format-bit-depth.png)

第一个下拉菜单可用于指定当前输出映射的文件格式。

第二个下拉列表用于指定输出映射的位深度。 位深度取决于所选的文件格式。 有关更多详细信息，请参阅[导出设置](export-settings.md)。

>[!NOTE]
>
> 要在导出时考虑格式和位深度设置，请确保将常规设置中的文件类型设置为&#x200B;**基于输出模板**。

## 源映射列表

![](../../assets/export-map-list.png)

### 输入图

输入图列表将可以通过[纹理集设置](../../interface/texture-set/texture-set-settings.md)添加的所有频道重新分组。

>[!NOTE]
>
> **用户**&#x200B;通道基于其原始名称（**用户\_x**），自定义名称将被忽略。

### 网格图

网格图是烘焙的纹理：

| 名称 | 描述 |
| --- | --- |
| **正常** | 烘焙的法线图。 |
| **世界空间法线** | 烘焙的世界空间法线。 |
| **ID** | 烘焙ID。 |
| **Ambient occlusion** | ambient occlusion |
| **弯曲** | 烘焙的弯曲。 |
| **位置** | 烘焙位置。 |
| **Thickness** | 烘焙的Thickness。 |
| **Height** | 烘焙的Height。 |
| **Bent normals** | 烘焙的bent normals。 |

### Converted maps

转换后的映射是由应用程序从其他源生成的映射：

| 名称 | 描述 |
| --- | --- |
| **Normal OpenGL** | 烘焙法线和纹理集法线法线图的OpenGL格式的组合通道。 |
| **Normal DirectX** | 以烘焙法线和纹理集法线法线图的DirectX格式表示的组合声道。 |
| **混合AO** | ambient occlusion和纹理集ambient occlusion频道的组合ambient occlusion。 |
| **Diffuse** | 从&#x200B;**Base color**&#x200B;和&#x200B;**金属**&#x200B;通道生成的Diffuse纹理（金属区域将替换为黑色）。 |
| **Specular** | 从&#x200B;**Base color**&#x200B;和&#x200B;**金属**&#x200B;频道生成的Specular纹理。 |
| **光泽度** | 从纹理的反转生成的粗糙度通道。 |
| **Unity4Diffuse** | 已弃用。 从&#x200B;**Base color**&#x200B;渠道生成的Diffuse纹理以匹配Unity 4着色器。 |
| **Unity4光泽** | 已弃用。 从&#x200B;**粗糙度**&#x200B;和&#x200B;**金属**&#x200B;声道生成的光泽度纹理，以匹配Unity 4着色器。 |
| **反射** | 白色表示介质材料的纹理，其他颜色表示为金属材料。 |
| **1/i或** | 包含1除以&#x200B;**IOR**&#x200B;值的纹理。 **IOR**&#x200B;从金属映射生成：1.4表示电介质，100表示金属（黑色）。 |
| **光泽度<sup>2</sup>** | **光泽度**&#x200B;声道的方形版本(**光泽度** \* **光泽度**) |
| **f0** | 包含菲涅耳0作为反射率值的纹理（介电系数为0.04，金属系数为1.0）。 |
