---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/scripting-and-development/api-reference/shader-api/shaders-shader-api/toon-shader-api.html"
breadcrumb-title: ''
description: 访问Substance 3D Painter的卡通着色器 API参考以创建自定义卡通样式渲染效果。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > API Reference > Shader API > Shaders - Shader API > Toon - Shader API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Toon -着色器 API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---


# Toon -着色器 API

## 基本卡通着色器

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


我们&#x200B;**绑定**&#x200B;**网格曲率**&#x200B;到我们的统一&#x200B;**曲率\_tex**。 如果没有可用的曲率，则会提供透明纹理。

```
//: param auto texture_curvature 

uniform SamplerSparse curvature_tex;
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


无论我们是否喜欢使用曲率。

```
//: param custom { 

//:   "default": false, 

//:   "label": "Use curvature" 

//: } 

uniform bool use_curvature;
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


**优先级**&#x200B;用于执行&#x200B;**轮廓检测**。 允许用户选择是否偏好使用曲率映射进行轮廓检测。

```
  if (use_curvature) { 

    float curv = textureSparse(curvature_tex, inputs.sparse_coord).r; 

    NdV = 1.0 - curv; 

  }
```


如果达到轮廓条件，则以黑色退出。

```
  if (NdV < mix(unlit_outline_thickness, lit_outline_thickness, NdL)) { 

    return; 

  }
```


在这里，我们将对颜色执行4步离散化。

```
  vec3 color = getBaseColor(basecolor_tex, inputs.sparse_coord); 

  if (NdL > 0.75) { 

    color = color; 

  } else if (NdL > 0.5) { 

    color = color * 0.5; 

  } else if (NdL > 0.1) { 

    color = color * 0.1; 

  } 

  else
```


后备是黑色的。

```
    color = vec3(0.0); 

 

  diffuseShadingOutput(color); 

} 

 
```
