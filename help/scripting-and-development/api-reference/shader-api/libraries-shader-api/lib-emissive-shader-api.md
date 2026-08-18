---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/scripting-and-development/api-reference/shader-api/libraries-shader-api/lib-emissive-shader-api.html"
breadcrumb-title: ''
description: 访问Substance 3D Painter的库放射性着色器 API参考，以创建放射状材质和发光效果。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > API Reference > Shader API > Libraries - Shader API > Lib Emissive - Shader API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lib Emissive -着色器 API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 0%

---


# Lib Emissive -着色器 API

## lib-emissive.glsl

**公共函数：** *pbrComputeEmissive*

从库导入

```
import lib-sparse.glsl
```


发射通道纹理。

```
//: param auto channel_emissive 

uniform SamplerSparse emissive_tex;
```


用于微调发射强度的值。

```
//: param custom { 

//:   "default": 1.0, 

//:   "label": "Emissive Intensity", 

//:   "min": 0.0, 

//:   "max": 100.0, 

//:   "group": "Common Parameters" 

//: } 

uniform float emissive_intensity;
```


计算观看者眼睛的发射亮度

```
vec3 pbrComputeEmissive(SamplerSparse emissive, SparseCoord coord) 

{ 

  return emissive_intensity * textureSparse(emissive, coord).rgb; 

} 

 
```
