---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/interface/shader-settings.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中配置着色器设置，以自定义素材渲染和视觉外观。
helpx_creative_field: ""
helpx_description: Painter > Interface > Shader settings
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 着色器设置
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 1%

---


# 着色器设置

![](../../assets/shader-settings.png)

**着色器设置**&#x200B;窗口允许控制着色器（和Iray mdl）参数和几何位移参数。

着色器是一个函数，用于定义在与视区中的光照和阴影交互时对象的外观。 在此应用程序中，着色器用于了解如何读取纹理集通道并在视区中渲染3D网格。

## 撤消栈栈和着色器文件

![](../../assets/shader-undo.png)

“着色器设置”窗口的此部分控制处理着色器时的主要参数。\
着色器的“撤消”/“重做”栈栈独立于主[“历史记录”](https://substance3d.adobe.com/display/DRAFTPAINTER/History)，以便在绘画时不会产生冲突。

如果着色器文件被标记为“过时”，建议尽可能更新它。 请参阅： [更新着色器](https://substance3d.adobe.com/display/DRAFTPAINTER/Updating+a+Shader)

| *设置* | *描述* |
| --- | --- |
| **撤消** | 恢复/取消对着色器文件的更改或任何着色器参数的修改 |
| **重做** | 再次应用通过撤消操作取消的更改。 |
| **着色器文件** | 显示当前使用的着色器文件的按钮。 单击按钮以打开迷你搁板并选择其他着色器。 |
| **实例名称** | 着色器实例的名称。 |
| **还原默认值** | 将所有着色器参数恢复为默认值（与着色器文件中的值相同）。 |

### 着色器实例

着色器实例是基于原始着色器文件但具有自定义参数的着色器。 可以在纹理集之间共享着色器实例，且纹理集可以具有唯一的着色器实例。

**例如：**&#x200B;项目可以使用基础着色器，而一个纹理集使用自定义着色器来支持不透明度。

要创建和管理着色器实例，请参阅[纹理集列表](../texture-set/texture-set-list.md)窗口。

## 着色器参数

![](../../assets/shader-parameters-1.png)

着色器参数取决于当前加载的着色器文件。

## 位移和镶嵌

![](../../assets/disp-parameters.png)

“位移”和“镶嵌”是可用于修改对象形状以添加更多细节的两项功能。

* **位移**：根据输入通道推移或偏移几何图形。
* **网格化**：细分几何以使其变密。 密度越大，多边形间距越短，细节也就越精细。

名为“**Height为正常**”的筛选器在盘架中可用，可用于获取最终正常映射（在本机转换不够强的情况下）。

### 位移

以下是位移设置：

| *设置* | *描述* |
| --- | --- |
| <b>源频道</b> | 网格变形所基于的通道。 默认值为Height，但也可以设置为位移。 |
| <b>缩放单位</b> | 选择定义位移比例的方式：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>规范化： </b>位移缩放相对于网格的定界框大小。</li> <li data-preserve-html="true"><b>场景： </b>位移比例相对于导入的场景文件的单位。</li> <li data-preserve-html="true"><b>物理尺寸(cm)</b>：基于对象物理尺寸以cm为单位测量位移比例。</li> </ul> |
| <b>缩放量</b> | 根据选定的缩放单位控制应用于项目中网格的变形量。 |

>[!NOTE]
>
> <b>场景</b>和<b>物理尺寸（厘米）</b>缩放单位设置都要求已准备好导入的模型进行物理尺寸测量。 如果在导入的文件中未正确设置单位，或者导入的文件类型不支持物理尺寸单位，则位移仍然有效，但可能无法根据需要提供准确的结果。

### 曲面细分

下面是“镶嵌”设置：

| *设置* | *描述* |
| --- | --- |
| **细分模式** | 确定如何计算细分量。 可用配置包括：<ul data-preserve-html="true"><li data-preserve-html="true"> 一致（默认） </li><li data-preserve-html="true"> Edge Length </li></ul> |
| **细分计数** | （模式一致）从1到32。 较高的值可生成更多多边形，从而提供更多细节，但可能会引发性能问题。 |
| **最大长度** | （模式边长度）1 /值。 将每个多边形边缘分割，直到每段都等于或小于该数值，即1/1为场景的大小。 |
