---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/scripting-and-development/api-reference/shader-api/parameters-shader-api/layering-bind-materials-shader-api.html"
breadcrumb-title: ''
description: 访问Substance 3D Painter的“分层绑定材料着色器 API”参考来在分层工作流中绑定材料。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > API Reference > Shader API > Parameters - Shader API > Layering Bind Materials - Shader API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 分层绑定材料-着色器 API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---


# 分层绑定材料-着色器 API

## 材料分层：将材料绑定为着色器参数

材料由唯一标识符“id”定义。 其他参数：

* &#39;default&#39;：要使用的默认材料资源名称。
* “size”：材料映射的纹理大小。
* “组”：材料选择小组件的UI组。

示例：

```
//:  materials [ 

//:    { 

//:       "id": "Material1", 

//:       "default": "Concrete 044", 

//:       "size": 512, 

//:       "group": "Material 1" 

//:    }, { 

//:       "id": "Material2", 

//:       "default": "Leaves elm", 

//:       "size": 1024, 

//:       "group": "Material 2" 

//:    } 

//:  ]
```


要将通道从材料绑定到取样器，请定义一个自动参数，该参数为材料的ID后跟通道标记（请参阅[all-channel-params.glsl](all-engine-params-shader-api.md)中的可用引擎）：

```
//: param auto Material1.channel_basecolor 

uniform sampler2D basecolor_tex1; 

//: param auto Material1.channel_metallic 

uniform sampler2D metallic_tex1; 

//: param auto Material1.channel_roughness 

uniform sampler2D roughness_tex1; 

 

//: param auto Material2.channel_basecolor 

uniform sampler2D basecolor_tex2; 

//: param auto Material2.channel_metallic 

uniform sampler2D metallic_tex2; 

//: param auto Material2.channel_roughness 

uniform sampler2D roughness_tex2; 

 
```
