---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/getting-started/project-creation.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中创建新项目以开始在3D模型上绘制纹理。
helpx_creative_field: ""
helpx_description: Painter > Getting Started > Project Creation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 项目创建
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '1157'
ht-degree: 1%

---


# 项目创建

![](../assets/v12_banner_project_window.jpg)

通过<b>“新建项目”窗口</b>，可创建项目文件以存储3D模型及其纹理信息。

根据在导入的3D模型上找到的材质定义，创建新的[纹理集](../interface/texture-set/texture-set.md)。 这意味着如果多个对象具有不同的材质，则可以通过单个文件导入这些对象（即使使用重叠的UV）。

## 创建新项目

要创建新项目，请单击<b>文件>新建</b>或使用键盘快捷键<b>Ctrl + N</b>。

以下是“新建项目”窗口中所有可用参数的说明。

### 基本设置

| *参数* | *描述* |
| --- | --- |
| **文件** | 单击“选择”按钮以指定要载入的3D模型文件。 [此处提供了支持的文件格式列表。](https://experienceleague.adobe.com/zh-hans/docs/substance-3d/general-knowledge/ecosystem/import-and-export-formats) |
| **模板** | 指定将定义项目默认设置的模板。 模板包含以下参数：<ul data-preserve-html="true"> <li data-preserve-html="true">纹理集设置。</li> <li data-preserve-html="true">显示设置。</li> <li data-preserve-html="true">烘焙设置。</li> <li data-preserve-html="true">着色器资源（包括连接的纹理）。</li> <li data-preserve-html="true">环境映射文件。</li> </ul>  **注意：**&#x200B;模板是<b>\*.spt</b>文件，通过[文件菜单](../interface/main-menu/file-menu.md)从现有项目创建并保存在Assets文件夹中以便与团队成员轻松共享。 |
| <b>分辨率</b> | 为每个纹理集定义项目的默认纹理分辨率。 在应用程序内工作时，分辨率可以高达4K（4096x4096像素），而在导出时，分辨率可以高达8K（8192x8192像素）。 稍后可以通过[纹理集设置](../interface/texture-set/texture-set-settings.md)随时更改分辨率。  **注意：** 8K导出至少需要2.5 GB的GPU空间才能使用VRam。 |

### 文件类型特定设置

选择USD后，其他文件类型特定的设置将变为可用。

| *参数* | *描述* |
| --- | --- |
| <b>作用域和变体</b> | 选择USD文件的特定部分。 默认情况下，此选项设置为“Root”，这意味着将使用整个USD文件创建Painter项目。  <b>更改……</b>将打开一个新窗口，其中显示USD的内容。 如果检测到变体，则可以选择用于项目创建的特定变体。 在[项目配置](../interface/project-configuration.md)设置中创建项目后可以更改范围和变型。 请注意 — <ul data-preserve-html="true"> <li data-preserve-html="true">只有建模变体选择会对项目产生任何影响。</li> <li data-preserve-html="true">当前未检测到嵌套在变体中的变体。</li> </ul> |
| <b>细分级别</b> | 对于应细分的几何，此设置允许您指定希望在Painter中对网格进行多少次细分，以便为其添加纹理。 如果在USD文件中将subdivision明确设置为“none”，则此设置将灰显。  细分在UV展开之后应用，因此这不会改变网格UV的形状。 在[项目配置](../interface/project-configuration.md)设置中创建项目后可以更改细分级别。 |
| <b>帧</b> | 对于检测到动画的USD文件，此设置允许您选择将用于创建Painter项目的帧。 如果选定的美元文件中没有动画，此设置将灰显。 在[项目配置](../interface/project-configuration.md)设置中创建项目后可以更改框架。 |

### 高级设置

| *参数* | *描述* |
| --- | --- |
| **法线贴图格式** | 定义项目的法线贴图格式，可以是<ul data-preserve-html="true"><li data-preserve-html="true"><strong>DirectX</strong> (X+、Y-、Z+)</li><li data-preserve-html="true"><strong>OpenGL</strong> (X+、Y+、Z+)</li></ul>  **注意：**&#x200B;作为提醒：<ul data-preserve-html="true"> <li data-preserve-html="true">默认情况下，<b>不实引擎</b>使用DirectX。</li> <li data-preserve-html="true">默认情况下，<b>Unity</b>使用OpenGL。</li> </ul> |
| **计算每个片段的正切空间** | 如果启用，将在片段（像素）着色器（而不是顶点着色器）中计算双边。 此参数影响视区中着色器解码法线映射的方式。 更改此设置将需要重新生成法线图。  **注意：**&#x200B;作为提醒：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>虚引擎</b>需要启用此设置。</li> <li data-preserve-html="true"><b>Unity</b>需要禁用此设置（如果您使用的是HDRP工作流程，则需启用此设置）</li> </ul> |

### UV 平铺设置 (UDIM)

>[!NOTE]
>
> 创建项目后，无法修改这些设置。

| *参数* | *描述* |
| --- | --- |
| **使用UV磁贴工作流程** | 如果选中，将对导入的网格进行不同的处理，以允许在一般UV范围(0-1)之外进行绘制。 使用UDIM的项目应启用此设置。 网格的处理可能因设置而异。   有关详细信息，请参阅[UV磁贴文档](../features/uv-tiles/uv-tiles.md)。 |
| <b>保留每个材质的UV拼贴布局并启用跨拼贴绘画</b> | 根据网格上的材料指定导入UV拼贴(UDIM)并进行分组。 这意味着单个纹理集可以包含2D视图中并排可见的多个UV拼贴。 位于同一纹理集中的UV磁贴可以无缝涂抹。  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r2-column-c1_image_copy" src="../assets/uvtiles-paintacross.jpg" width="500px"/></div> |
| <b>将UV拼贴转换为单独的纹理集（旧版）</b> | UV拼贴(UDIM)被分离为单独的纹理集并被重命名，同时忽略任何材质指定。 每个UV拼贴都移动到UV [0-1]范围以便进行绘制。  <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table2_row-r3-column-c1_image" src="../assets/uvtiles-legacy.jpg" width="500px"/></div> |

### 导入设置

| ***参数*** | ***描述*** |
| --- | --- |
| **导入相机** | 如果网格文件中存在摄像机，则摄像机将导入项目，可作为可视化预设进行访问。  **注意：** Substance 3D Painter在某些情况下不支持某些相机：<ul data-preserve-html="true"><li data-preserve-html="true">3DS Max中的物理摄像头</li><li data-preserve-html="true">存储在Alembic文件中的正交相机(&#42;.abc)。</li></ul> |
| **自动展开** | 如果启用，则将生成导入网格上缺少的UV。 根据通过&#x200B;**选项**&#x200B;按钮选择的设置，处理可能会更改。有关详细信息，请参阅[自动UV解包文档](../features/automatic-uv-unwrapping.md)。 |

### 导入烘焙贴图

使用<b>添加</b>按钮将纹理文件加载为网格图，并在[纹理集设置](../interface/texture-set/texture-set-settings.md)中自动分配这些文件。 必须遵循特定的命名约定，才能将网格映射自动指定给其“纹理集”。 也可以直接在应用程序内烘焙网格图；请参阅烘焙文档。

命名约定： <b> TextureSetName\_MeshMapName</b>

示例： <b> DefaultMaterial\_ambient\_遮蔽.png </b>

支持的网格映射及其命名列表：

| *网格图* | *文件名约定* |
| --- | --- |
| **环境遮蔽** | 环境遮蔽 |
| **曲率** | 曲率 |
| **正常** | normal\_base |
| **世界空间正常** | world\_space\_normals |
| **ID** | id |
| **位置** | 位置 |
| **Thickness** | 厚度 |

### 实际大小

物理尺寸设置允许您调整Painter确定网格在真实世界单位中的物理尺寸的方式。 这对于确保以逼真的比例应用材质非常有用。

* 使用网格文件的内部单位比例：大多数文件类型包括有关从3D建模应用程序导出的对象物理尺寸的信息。 选中此选项后，Painter将使用导入文件中的此信息。
* 自定单位比例：覆盖导入文件的单位比例，或者如果未包括单位比例，则使用自定输入框调整单个“单位”的大小。
* 分配材质时，将填充图层缩放切换为物理尺寸：如果启用此选项，则具有物理尺寸信息的材质可以调整其缩放，以匹配它们所应用到的表面的物理尺寸。

### 色彩管理

![](../assets/newproj-cm.png)

此部分控制项目的色彩管理设置。 默认情况下，它设置为旧版（sRGB/线性工作流）。

查看[色彩管理](../features/color-management/color-management.md)文档，详细了解如何使用此工作流程以及这些设置的作用。
