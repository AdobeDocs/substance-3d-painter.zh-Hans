---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/scripting-and-development/api-reference/shader-api/libraries-shader-api/lib-random-shader-api.html"
breadcrumb-title: ''
description: 访问Substance 3D Painter的Lib Random着色器 API参考，以便在自定义着色器开发中生成随机值。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > API Reference > Shader API > Libraries - Shader API > Lib Random - Shader API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 库随机 — 着色器 API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# 库随机 — 着色器 API

## lib-random.glsl

**公共函数：** *getBlueNoiseThreshold* *getBlueNoiseThresholdTemporal* *fibonacci1D* *fibonacci2D* *fibonacci2DDitheredTemporal*

从库导入

```
import lib-defines.glsl
```


包含标量值的2D蓝色杂色纹理

```
//: param auto texture_blue_noise 

uniform sampler2D texture_blue_noise;
```


蓝色杂色纹理分辨率

```
const ivec2 texture_blue_noise_size = ivec2(256);
```


当前帧随机植入

```
//: param auto random_seed 

uniform int alg_random_seed;
```


基于像素坐标获取统一的随机值。

```
float getBlueNoiseThreshold() 

{ 

  return texture(texture_blue_noise, gl_FragCoord.xy / vec2(texture_blue_noise_size)).x + 0.5 / 65536.0; 

}
```


基于像素坐标和帧ID获取统一的随机值。

```
float getBlueNoiseThresholdTemporal() 

{ 

  return fract(getBlueNoiseThreshold() + M_GOLDEN_RATIO * alg_random_seed); 

}
```


从fibonacci序列返回i *th*&#x200B;编号。

```
float fibonacci1D(int i) 

{ 

  return fract((float(i) + 1.0) * M_GOLDEN_RATIO); 

}
```


返回fibonacci序列中的i *th*&#x200B;对。 需要nbSample才能得到均匀分布。

```
vec2 fibonacci2D(int i, int nbSamples) 

{ 

  return vec2( 

    (float(i)+0.5) / float(nbSamples), 

    fibonacci1D(i) 

  ); 

}
```


返回fibonacci序列中的i *th*&#x200B;对。 需要nbSample才能得到均匀分布。 此版本应用了每帧和每像素伪随机旋转。

```
vec2 fibonacci2DDitheredTemporal(int i, int nbSamples) 

{ 

  vec2 s = fibonacci2D(i, nbSamples); 

  s.x += getBlueNoiseThresholdTemporal(); 

  return s; 

} 

 
```
