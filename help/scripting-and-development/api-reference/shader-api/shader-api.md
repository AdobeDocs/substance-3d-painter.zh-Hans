---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/scripting-and-development/api-reference/shader-api.html"
breadcrumb-title: ''
description: 访问Substance 3D Painter的着色器 API参考，以创建自定义着色器并扩展渲染功能。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > API Reference > Shader API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 着色器 API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '702'
ht-degree: 0%

---


# 着色器 API

![](../../../assets/header-shader.jpg)

Substance Painter使用着色器在其实时视口中渲染材质。 可以编写自定义着色器以实现新行为，或简单地使视区与其他渲染器匹配。

在[Substance share](https://share.allegorithmic.com/libraries?by_category_type_id=6)上可以找到其他用于Substance Painter的着色器。

>[!NOTE]
>
> 通过转到菜单&#x200B;**“帮助”>“文档”>“着色器 API”**，也可以直接从应用程序使用该着色器 API。

## 着色器引用

## 更改日志

* [完整更改日志文件](changelog-shader-api.md)

## Warm up

在Substance Painter中，您可以在&#x200B;*GLSL*&#x200B;中编写自己的着色器。 我们仅允许您写入碎片着色器的&#x200B;*部分*，它有时称为&#x200B;*表面着色器*。 我们不用再费力了，来介绍“Hello world”Substance Painter表面着色器：

```
void shade(V2F inputs) { 

  diffuseShadingOutput(vec3(1.0, 0.0, 1.0)); 

}
```


现在，如果您将此片段保存到&#x200B;*.glsl*&#x200B;文件中，并通过将其拖放到层架的“着色器”选项卡中将其加载到Substance Painter中，您现在可以使用它并在网格上看到漂亮的统一粉红色。

## 表面着色器

* [surface-shader.glsl](shaders-shader-api/surface-shader-shader-api.md)

## 引擎提供的数据（或者如何访问我的频道？）

在Substance Painter中，您可以访问渲染引擎参数（文档的通道、其他纹理、与相机相关的数据等）。 以下是引擎提供的所有参数的详尽列表：

* [all-engine-params.glsl](parameters-shader-api/all-engine-params-shader-api.md)

## 引擎设置（或者如何指定渲染状态？）

在某些情况下，您可能希望使用特定的渲染配置（剔除、混合、取样局部性等）来获得效果。 某些渲染状态是公开的，可以在着色器中设置。 以下是所有公开渲染状态的详尽列表：

* [all-rendering-states-params.glsl](parameters-shader-api/all-rendering-states-params-shader-api.md)

## 自定义调整（或者如何调整着色器？）

着色器中通常会有自定义的调整。 为了在Substance Painter的着色器中执行此操作，我们引入了一种指定自定义调整的方法。 以下是所有自定义着色器调整类型的详尽列表：

* [all-custom-params.glsl](parameters-shader-api/all-custom-params-shader-api.md)

## 嵌入式库

为了避免在所有着色器中编写大量的样板代码，我们创建了一个实用小函数库。 **请注意，您目前无法对其进行编辑或创建您自己的文件。**

* [lib-alpha.glsl](libraries-shader-api/lib-alpha-shader-api.md) ：包含不透明度相关帮助程序
* [lib-bayer.glsl](libraries-shader-api/lib-bayer-shader-api.md) ：包含bayer矩阵帮助程序
* [lib-defines.glsl](libraries-shader-api/lib-defines-shader-api.md) ：包含有用的数学常量
* [lib-emissive.glsl](libraries-shader-api/lib-emissive-shader-api.md) ：包含发射属性帮助程序
* [lib-env.glsl](libraries-shader-api/lib-env-shader-api.md) ：包含与环境映射相关的帮助程序
* [lib-normal.glsl](libraries-shader-api/lib-normal-shader-api.md) ：包含与正常映射相关的帮助程序（和Height映射生成的正常映射）
* [lib-pbr.glsl](libraries-shader-api/lib-pbr-shader-api.md) ：包含基于物理的渲染帮助程序
* [lib-pbr-aniso.glsl](libraries-shader-api/lib-pbr-aniso-shader-api.md) ：包含基于各向异性物理的渲染帮助程序
* [lib-pom.glsl](libraries-shader-api/lib-pom-shader-api.md) ：包含视差遮蔽映射帮助程序
* [lib-random.glsl](libraries-shader-api/lib-random-shader-api.md) ：包含随机实用程序（低差异序列）
* [lib-sampler.glsl](libraries-shader-api/lib-sampler-shader-api.md) ：包含通道getter帮助程序
* [lib-sparse.glsl](libraries-shader-api/lib-sparse-shader-api.md) ：包含安全稀疏纹理采样帮助程序
* [lib-sss.glsl](libraries-shader-api/lib-sss-shader-api.md) ：包含次表面散射帮助程序
* [lib-utils.glsl](libraries-shader-api/lib-utils-shader-api.md) ：包含颜色实用程序函数（sRGB转换、色调映射）
* [lib-vector.glsl](libraries-shader-api/lib-vectors-shader-api.md) ：包含公共矢量帮助程序

## 元数据

可以声明其他非必需信息，以便为渲染系统提供一些提示。 语法如下：

```
//: metadata { 

//:   "key1":"value1", 

//:   "key2":"value2" 

//: }
```


支持的密钥包括：

* **custom-ui**：将标准着色器参数用户界面替换为编写为QML模块的自定义视图（请参阅脚本文档）。 该路径可以是绝对路径，也可以是相对于您的托架&#x200B;*自定义UI*&#x200B;文件夹之一的路径。
* **mdl**：定义要与着色器一起使用的Iray mdl素材。 路径语法如下： *mdl：:folder1::folder2:：mdl\_filename：：material\_name*，其中&#x200B;*folder1：:folder2:：mdl\_filename*&#x200B;是您的托架&#x200B;*mdl*&#x200B;文件夹之一中指向mdl文件的路径，*：：material\_name*&#x200B;是此mdl文件中声明的材料的名称。 （例如： &quot;mdl&quot; ： &quot;mdl：:alg::materials:：physical\_metallic\_roughness：：physical\_metallic\_roughness&quot;）

## 着色器示例（终于见效了！）

为了尝一尝真正的着色器外观，这里有一些示例着色器，按增加的复杂性排序：

* [pixelated.glsl](shaders-shader-api/pixelated-shader-api.md) ：像素化着色器
* [toon.glsl](shaders-shader-api/toon-shader-api.md) ：卡通着色器
* [pbr-metal-rough.glsl](shaders-shader-api/pbr-metal-rough-shader-api.md) ：嵌入在Substance Painter中的默认PBR着色器

## 动态材质分层

该动态材质分层是一个特定的工作流程，其中材质在着色器中混合在一起，并且允许用户在Substance Painter中动态编辑混合蒙版。 要启用此工作流程，需要新增两项功能：

* 从着色器定义声明可编辑栈栈： [layering\_declare\_stacks.glsl](parameters-shader-api/layering-declare-stacks-shader-api.md)
* 将材质绑定为着色器参数： [layering\_bind\_materials.glsl](parameters-shader-api/layering-bind-materials-shader-api.md)
