---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/getting-started/export/creating-export-presets.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中创建自定义输出模板，以定义您自己的纹理导出配置。
helpx_creative_field: ""
helpx_description: Painter > Getting Started > Export > Creating Output templates
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 创建输出模板
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '963'
ht-degree: 0%

---


# 创建输出模板

本页介绍如何创建和修改自定义输出模板。 输出模板控制导出纹理的命名和配置。 创建自定义输出模板后，您可以配置导出以使其完全匹配您的工作流程。

导出窗口的“配置”选项卡分为三个主要部分：

* <b>预设列表：</b>（左）允许选择要编辑的模板，或复制和重命名现有模板。
* <b>输出纹理列表</b>：（中间）列出所选预设的内容，并显示命名约定和通道打包选项。
* <b>通道列表</b>和<b>转换的纹理</b>：（右）要用于合成导出纹理内容的通道和纹理列表。

![](../assets/image2018-4-25-13-36-44.png){width="800px"}

>[!NOTE]
>
> 输出模板作为<b>单个文件</b>保存在磁盘上，并且可以与Substance 3D Painter的任何其他用户共享。\
> 在[Substance 3D Painter文件](../pipeline-and-integration/resource-management/shelf-and-assets-location.md)的assets/export-presets文件夹中，可找到您创建的自定义模板的本地文件。

>[!NOTE]
>
> 当使用模板导出纹理时，模板文件会在后续保存时自动包含在项目文件中。\
> 这允许共享项目和/或将项目移动到另一台计算机，同时保留用于导出纹理的模板。\
> 项目中仅保存上次使用的预设。 但是，如果Substance 3D Painter检测到具有相同名称的预设，项目中的预设将在列表中标记为“已过时”。

## 创建模板

预设列表的顶部有三个按钮：

![](../assets/image2018-4-25-13-39-6.png)

* <b>复制</b> ：复制现有模板。
* <b>删除</b> ：删除任何选定的模板。
* <b>创建</b> ：创建一个新的空模板。

您也可以双击模板或<b>右键单击>重命名</b>以更改模板的名称。

## 创建输出映射

选择模板后，可以使用专用按钮（位于窗口中间部分的顶部）添加新输出映射。

![](../assets/output-buttons.png)

![](../assets/output-map.gif)

一旦创建了映射，就可以对其命名，然后将输入映射拖放到可用通道槽中。\
输入映射放入输出映射部分后，将打开一个菜单，询问在该插槽中加载哪种类型的内容。

选项范围从<b>RGB</b>和<b>单个</b>声道，到<b>Alpha</b>和输入的<b>灰度</b>转换。

>[!NOTE]
>
> 每次拖放输入映射时，将生成随机颜色。 这将为通道和加载的相应输入映射提供视觉提示。\
> 该按钮还指示插槽中加载了什么：
> 
> * 背景色：指示加载了哪些<b>输入</b>映射。
> * RGB栏：指示已加载输入映射中的<b>R</b> 、 <b>G</b>和<b>B</b>声道。
> * 红色条：指示已加载输入映射中的<b>红色</b>通道。
> * 绿色条：指示已加载输入映射中的<b>绿色</b>通道。
> * 蓝色条：指示已加载输入映射中的<b>蓝色</b>通道。
> * 灰色条：表示输入映射加载为<b>灰度</b>（从RGB到灰度转换，或者因为输入已处于灰度状态）。
> * 黑线/白线：指示已加载输入映射中的<b>alpha</b>通道。 在Substance 3D Painter中，输入中的Alpha与总绘制区域相对应。

## 命名输出映射

![](../assets/output-name.gif)

在导出过程中，可以使用某些标记自动生成纹理的名称。

* <b> $mesh</b> ：项目中加载的网格文件的名称
* <b> $textureSet</b> ：纹理集的名称
* <b> /</b>（正斜杠）：文件夹分隔

<b>示例</b> ：具有名为“MaterialBase”的纹理集的cymourai.fbx

* <b>$mesh\_$textureSet\_BaseColor</b>将生成<b>cymourai\_MaterialBase\_BaseColor.png。</b>
* <b>$mesh/$textureSet\_BaseColor</b>将生成一个名为<b>cymourai</b>的文件夹，其中包含名为<b>MaterialBase\_BaseColor.png</b>的纹理。

>[!NOTE]
>
> 如果导出格式设置为&#x200B;**PSD** (Photoshop)文件格式，则会自动将文件夹转换为组。

## 将通道分配给输出映射

![](../assets/empty-channel.gif)

可以使（输出映射的）某些通道完全空白。 在这种情况下，将分配默认颜色。

>[!NOTE]
>
> 如果槽指的是导出期间纹理集中不存在的通道，则还会生成默认颜色。\
> 此颜色根据提供最佳中性值的通道而变化。\
>  **示例** ：如果缺失，将使用默认的灰度值生成Height通道。

有不同类型的映射：

* <b>输入映射</b>：可在纹理集中添加的直接通道。 通过“纹理集”设置面板。
* <b>网格映射</b>：纹理集的附加映射槽中存在纹理（烘焙纹理）。
* <b>转换后的映射：</b>虚拟纹理，这些纹理在导出过程中根据文档中存在的通道生成。
  * <b>普通OpenGL/DirectX</b> ：通过组合附加映射中的普通、Height和普通通道，在专用空间中输出普通。
  * <b>混合AO</b>：将环境遮蔽附加映射与环境色遮蔽通道相结合。
  * <b>扩散</b>：从BaseColor和金属通道生成的扩散颜色（金属部分将替换为黑色）。
  * <b>Specular</b>：从BaseColor和金属色通道生成的Specular。
  * <b>光泽度</b>：粗糙度通道的反向。
  * <b>Unity4漫射</b>：从BaseColor生成漫射颜色以匹配Unity4着色器。
  * <b>Unity4光泽</b>：从粗糙度和金属色通道生成的光泽度以匹配Unity4着色器。
  * <b>反射</b>：导出白色表示介电材料和其他金属材料颜色的地图
  * <b>1/ior</b>： 1除以ior值，从金属结构图中生成ior：1.4（电介质），100(金属（黑色）)
  * <b>光泽度<sup>2</sup></b>：光泽度通道的方形版本（光泽度\*光泽度）
  * <b>f0</b>：菲涅耳0处的反射率值（电介质0.04，金属1.0）
