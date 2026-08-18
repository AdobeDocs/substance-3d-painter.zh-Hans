---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/scripting-and-development/api-reference/shader-api/libraries-shader-api/lib-sss-shader-api.html"
breadcrumb-title: ''
description: 访问Substance 3D Painter的Lib SSS着色器 API参考，以在自定义着色器中创建子表面散射效果。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > API Reference > Shader API > Libraries - Shader API > Lib SSS - Shader API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lib SSS -着色器 API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 0%

---


# Lib SSS -着色器 API

## lib-sss.glsl

**公共函数：** *getSSSCoefficients*

从库导入

```
import lib-sampler.glsl
```


标量SSS系数纹理

```
//: param auto channel_scattering 

uniform SamplerSparse sss_tex; 

 

//: param auto scene_original_radius 

uniform float sssSceneScale; 

 

//: param custom { 

//:   "label": "Enable", 

//:   "default": true, 

//:   "group": "Subsurface Scattering Parameters", 

//:   "description": "<html><head/><body><p>Enable the Subsurface Scattering. It needs to be activated in the Display Settings and a Scattering channel needs to be present for these parameters to have an effect.</p></body></html>" 

//: } 

uniform bool sssEnabled;
```


选择光线是直接透过材质（半透明）还是先扩散，然后再开始散点（皮肤）。

```
//: param custom { 

//:   "default": 1, 

//:   "label": "Scattering Type", 

//:   "widget": "combobox", 

//:   "values": { 

//:     "Translucent": 0, 

//:     "Skin": 1 

//:   }, 

//:   "group": "Subsurface Scattering Parameters", 

//:   "description": "<html><head/><body><p>Skin or Translucent/Generic. It needs to be activated in the Display Settings and a Scattering channel needs to be present for these parameters to have an effect.</p></body></html>" 

//: } 

uniform int sssType;
```


次表面散射效果的全局缩放

```
//: param custom { 

//:   "default": 0.5, 

//:   "label": "Scale", 

//:   "min": 0.01, 

//:   "max": 1.0, 

//:   "group": "Subsurface Scattering Parameters", 

//:   "description": "<html><head/><body><p>Controls the radius/depth of the light absorption in the material. It needs to be activated in the Display Settings and a Scattering channel needs to be present for these parameters to have an effect.</p></body></html>" 

//: } 

uniform float sssScale;
```


材料的SSS的波长依赖性

```
//: param custom { 

//:   "default": [0.701, 0.301, 0.305], 

//:   "label": "Color", 

//:   "widget": "color", 

//:   "group": "Subsurface Scattering Parameters", 

//:   "description": "<html><head/><body><p>The color of light when absorbed by the material. It needs to be activated in the Display Settings and a Scattering channel needs to be present for these parameters to have an effect.</p></body></html>" 

//: } 

uniform vec3 sssColor;
```


返回材质SSS系数

```
vec4 getSSSCoefficients(float scattering) { 

  if (sssEnabled) { 

    vec3 sss = sssScale / sssSceneScale * scattering * sssColor; 

    return vec4(sss, sss == vec3(0.0) ? 0.0 : 1.0); 

  } 

  return vec4(0.0); 

} 

vec4 getSSSCoefficients(SparseCoord coord) { 

  if (sssEnabled) { 

    return getSSSCoefficients(getScattering(sss_tex, coord)); 

  } 

  return vec4(0.0); 

} 

 
```
