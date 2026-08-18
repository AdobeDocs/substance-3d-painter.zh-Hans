---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/scripting-and-development/api-reference/shader-api/shaders-shader-api/pixelated-shader-api.html"
breadcrumb-title: ''
description: 访问Substance 3D Painter的像素化着色器 API参考以创建自定义像素化渲染效果。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > API Reference > Shader API > Shaders - Shader API > Pixelated - Shader API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 像素化 — 着色器 API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---


# 像素化 — 着色器 API

## 基本像素化着色器

从库导入。

```
import lib-sampler.glsl
```


我们定义全局光的位置

```
const vec3 light_pos = vec3(10.0, 10.0, 10.0);
```


我们&#x200B;**将**&#x200B;自动参数世界眼睛位置绑定到我们的制服&#x200B;**摄像机\_pos**。

```
//: param auto world_eye_position 

uniform vec3 camera_pos;
```


我们&#x200B;**绑定**&#x200B;文档的通道&#x200B;**基色**&#x200B;到统一的&#x200B;**basecolor\_tex**。

```
//: param auto channel_basecolor 

uniform SamplerSparse basecolor_tex;
```


我们将为此着色器定义新的自定义调整及其默认值。 此图层用于在着色时调整轮廓的Thickness。

```
//: param custom { 

//:  "default": 0.4, 

//:   "min": 0.0, 

//:   "max": 1.0, 

//:   "label": "Unlit outline thickness" 

//: } 

uniform float unlit_outline_thickness;
```


我们将为此着色器定义新的自定义调整及其默认值。 此滑块用于在光照时调整轮廓Thickness。

```
//: param custom { 

//:   "default": 0.1, 

//:   "min": 0.0, 

//:   "max": 1.0, 

//:   "label": "Lit outline thickness" 

//: } 

uniform float lit_outline_thickness;
```


着色器的入口点。

```
void shade(V2F inputs) 

{
```


我们计算出一些有用的值。

```
  vec3 V = normalize(camera_pos - inputs.position); 

  vec3 N = normalize(inputs.normal); 

  vec3 L = normalize(light_pos - inputs.position); 

  float NdV = dot(N, V); 

  float NdL = max(0.0, dot(N, L));
```


**优先级**&#x200B;用于执行&#x200B;**轮廓检测**。 如果达到轮廓条件，则以黑色退出。

```
  if (NdV < mix(unlit_outline_thickness, lit_outline_thickness, NdL)) { 

    return; 

  } 

 

  vec3 baseColor = getBaseColor(basecolor_tex, inputs.sparse_coord);
```


基于基色明亮度，在蒙版大小中引入一些抖动

```
  float maskRadiusJitter = pow(dot(baseColor, vec3(0.3333)), 0.1);
```


根据片段的屏幕空间位置计算掩码值。 这将创建一个类似图案的网格。

```
  float mask = pow(1.0 - length(fract(gl_FragCoord.xy / 7.0) - vec2(0.5)), maskRadiusJitter * 5.0) * 5.0;
```


这里，我们对基色进行取样，并应用简单的扩散衰减

```
  vec3 color = baseColor * NdL; 

 

  diffuseShadingOutput(mask * color); 

} 

 
```
