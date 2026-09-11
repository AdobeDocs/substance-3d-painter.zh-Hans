---
helpx_url: 'https://helpx.adobe.com/substance-3d-painter/interface/project-configuration.html'
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中配置项目设置，以设置纹理分辨率、通道和项目属性。
helpx_creative_field: ''
helpx_description: Painter > Interface > Project configuration
helpx_experience_level: ''
helpx_learn_topic: ''
helpx_tags: ''
title: 项目配置
user-guide-description: ''
user-guide-title: ''
source-git-commit: 3e4ef9bd5897f042b01d6c0819ec06cc21ba208a
workflow-type: tm+mt
source-wordcount: '839'
ht-degree: 3%

---


# 项目配置

![](../assets/project-configuration-full.png)

“项目配置”窗口包含用于修改项目设置的控件。 项目设置通常在创建新项目时设置，但有时可能需要在项目后期对这些设置进行更改。

## 3D 网格

如果对3D 网格或网格文件进行了更改，您可以重新导入网格，同时仍保留其他项目数据。 检查&#x200B;**重新导入网格**，并确保正在导入正确的文件。

在需要执行以下操作时，重新导入网格通常很有用：

* 更新3D模型拓扑
* 更新UV
* 添加或删除[纹理集](texture-set/texture-set.md)

| **参数** | **描述** |
| --- | --- |
| **3D 网格** | 指示3D模型文件的路径。 使用&#x200B;**选择按钮**&#x200B;更改项目的源文件。 |
| **重新导入网格** | 如果启用，则单击界面底部的“确定”时将重新导入网格文件。 如果“选择”按钮用于指定不同于原始网格文件的网格文件，则会自动检查此参数。 |

>[!NOTE]
>
> 如果在重新导入项目网格时材料ID发生更改或被重命名，则项目中以前的纹理集可能会变为禁用状态，从而显示为缺失纹理。 此问题可通过&#x200B;**纹理集列表**&#x200B;中的[重新分配窗口](texture-set/texture-set-reassignment.md)修复。

## 项目设置

此部分控制多个与项目相关的设置：

<table>
  <tr>
    <th><em>设置</em></th>
    <th><em>描述</em></th>
  </tr>
  <tr>
    <td><strong>法线图格式</strong></td>
    <td>定义在视口中用于网格的法线图的格式。 此参数仅影响视口中的<a href="shader-settings/shader-settings.md">着色器</a>和<a href="../baking/baking.md">Baker</a>中的网格图。 该图层堆叠是独立的。 对于常见应用程序建议的值：<br><br><ul><li><strong>Unity</strong>： OpenGL</li><li><strong>虚构引擎</strong>：DirectX</li><li><strong>Maya</strong>： OpenGL</li><li><strong>3DS最大值</strong>：DirectX</li><li><strong>混合器</strong>： OpenGL</li></ul></td>
  </tr>
  <tr>
    <td><strong>逐插件碎片计算切线空间</strong></td>
    <td>确定如何在视口中计算和显示着色和光照法线图。 如果启用，将按像素而不是按顶点计算网格的正切和二项式。<br>对于常见应用程序的推荐值：<br><br><ul><li><strong>Unity</strong>：已禁用（如果使用HDRP则启用）</li><li><strong>虚构引擎</strong>：已启用</li></ul></td>
  </tr>
</table>

>[!NOTE]
>
> 更改普通计算或正切格式需要重新烘焙网格图，以确保视口中的外观正确无误。

### 文件类型特定设置

选择网格格式后，其他文件类型特定的设置将变为可用。

![](../assets/image2023-1-30-11-16-6.png){width="473px"}

<table>
  <tr>
    <th><em>参数</em></th>
    <th><em>描述</em></th>
  </tr>
  <tr>
    <td><strong>范围和变体</strong></td>
    <td>选择USD文件的特定部分。 默认情况下，它设置为“根”，这意味着整个USD文件都将在Painter项目中使用。 <strong>更改……</strong>将打开一个新窗口，其中显示USD的内容。 如果检测到变体，您可以选择特定的变体加载到项目中。<br><br>注意：<br><ul><li>只有建模变量选择才会产生任何影响。</li><li>当前未检测到嵌套在变体中的变体。</li></ul></td>
  </tr>
  <tr>
    <td><strong>细分级别</strong></td>
    <td>适用于具有细分的几何图形。 指定在Painter中为纹理工具对网格进行多少细分。 如果在USD文件中将细分明确设置为“无”，则此设置将灰显。 细分在展开之后应用，因此不会改变网格UV的形状。</td>
  </tr>
  <tr>
    <td><strong>框架</strong></td>
    <td>适用于检测动画的美元。 选择将加载到Painter项目的帧。 如果选定的USD文件中没有动画，此设置将灰显。</td>
  </tr>
</table>

## UV 平铺设置

此部分包含用于切换项目中的UDIM使用的控件。 不能在创建项目后更改这些设置，但可以在此处查看项目的设置。 有关详细信息，请参阅[UV 平铺文档](../features/uv-tiles/uv-tiles.md)。

## 导入设置

这些设置控制所选网格的导入方式：

| *设置* | *描述* |
| --- | --- |
| **导入相机** | 如果启用，则还会导入网格文件中的相机，并且这些文档在3D视口中可用。 |
| **保留网格上的描边位置** | 此设置控制导入新3D 网格后重新计算画笔描边的方式。 大多数情况下，建议保持启用此设置。 有关更多详细信息，请参阅[UV重新投影](../features/uv-reprojection.md)文档。 |
| **自动展开** | 自动展开。 单击“选项”按钮以配置该过程。 有关详细信息，请参阅[自动展开文档](../features/automatic-uv-unwrapping.md)。 |

### 物理尺寸设置

调整已导入网格的[物理尺寸](../features/physical-size.md)。

| *设置* | *描述* |
| --- | --- |
| **使用网格文件的内部单位比例** | 如果网格是使用物理上准确的度量值创建的，则选择此选项，以在Painter中保持相同的物理尺寸。 |
| **自定义单位比例** | 如果创建网格时没有考虑物理尺寸，请使用此选项自定义网格的大小。 您需要了解所导入网格的所需物理尺寸和大小（以单位表示），才能确定此值。 |
| **分配填充图层时，将材料缩放切换为物理尺寸** | 启用后，填充图层和效果将在分配具有物理尺寸属性的材料时自动将缩放方法切换为物理尺寸。 |

### 色彩管理设置

本节控制有关如何转换颜色的设置。 有关详细信息，请参阅[色彩管理](../features/color-management/color-management.md)文档。
