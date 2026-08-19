---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/scripting-and-development/api-reference/shader-api/libraries-shader-api/lib-utils-shader-api.html"
breadcrumb-title: ''
description: 请访问Substance 3D Painter的Lib Utils着色器 API参考，以便在自定义着色器开发中使用实用程序函数。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > API Reference > Shader API > Libraries - Shader API > Lib Utils - Shader API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lib实用程序 — 着色器 API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---


# Lib实用程序 — 着色器 API

## Allegorithmic实用程序函数

## 色调映射

下面是您可以在着色器中使用的色调映射示例。 Painter不应用任何色调映射，但Yebis应用的可选色调映射除外。 如果您决定在着色器中执行某些色调映射，则会在Yebis色调映射之前应用该映射。

根据参数sigma和n执行S曲线色调映射。

```
vec3 tonemapSCurve(vec3 value, float sigma, float n) 

{ 

  vec3 pow_value = pow(value, vec3(n)); 

  return pow_value / (pow_value + pow(sigma, n)); 

}
```


## sRGB转换

这些是Painter中使用的转换。 您可以通过在自定义着色器中放置以下线条来覆盖视区中的自动线性 — > sRGB转换：

*#define DISABLE\_FRAMEBUFFER\_SRGB\_CONVERSION*

以及进行您自己的自定义转换。

sRGB到线性颜色转换。 标量版本。

```
float sRGB2linear(float x) 

{ 

  return x <= 0.04045 ? 

    x * 0.0773993808 : // 1.0/12.92 

    pow((x + 0.055) / 1.055, 2.4); 

}
```


sRGB到线性颜色转换。 RGB版本。

```
vec3 sRGB2linear(vec3 rgb) 

{ 

  return vec3( 

    sRGB2linear(rgb.r), 

    sRGB2linear(rgb.g), 

    sRGB2linear(rgb.b)); 

}
```


sRGB到线性颜色转换。 RGB+Alpha版本。

```
vec4 sRGB2linear(vec4 rgba) 

{ 

  return vec4(sRGB2linear(rgba.rgb), rgba.a); 

}
```


线性到sRGB颜色转换。 标量版本。

```
float linear2sRGB(float x) 

{ 

  return x <= 0.0031308 ? 

      12.92 * x : 

      1.055 * pow(x, 0.41666) - 0.055; 

}
```


线性到sRGB颜色转换。 RGB版本。

```
vec3 linear2sRGB(vec3 rgb) 

{ 

  return vec3( 

      linear2sRGB(rgb.r), 

      linear2sRGB(rgb.g), 

      linear2sRGB(rgb.b)); 

}
```


线性到sRGB颜色转换。 RGB+Alpha版本。

```
vec4 linear2sRGB(vec4 rgba) 

{ 

  return vec4(linear2sRGB(rgba.rgb), rgba.a); 

}
```


线性到sRGB颜色转换可选。 标量版本。

```
//: param auto conversion_linear_to_srgb 

uniform bool convert_to_srgb_opt; 

float linear2sRGBOpt(float x) 

{ 

  return convert_to_srgb_opt ? linear2sRGB(x) : x; 

}
```


线性到sRGB颜色转换可选。 RGB版本。

```
vec3 linear2sRGBOpt(vec3 rgb) 

{ 

  return convert_to_srgb_opt ? linear2sRGB(rgb) : rgb; 

}
```


线性到sRGB颜色转换可选。 RGB+Alpha版本。

```
vec4 linear2sRGBOpt(vec4 rgba) 

{ 

  return convert_to_srgb_opt ? linear2sRGB(rgba) : rgba; 

}
```


颜色转换。 标量版本。

```
uniform int output_conversion_method; 

float convertOutput(float x) 

{ 

 if (output_conversion_method == 0) return x; 

 else if (output_conversion_method == 1) return linear2sRGB(x); 

 else return sRGB2linear(x); 

}
```


颜色转换。 RGB版本。

```
vec3 convertOutput(vec3 rgb) 

{ 

 if (output_conversion_method == 0) return rgb; 

 else if (output_conversion_method == 1) return linear2sRGB(rgb); 

 else return sRGB2linear(rgb); 

}
```


颜色转换。 RGB+Alpha版本。

```
vec4 convertOutput(vec4 rgba) 

{ 

 if (output_conversion_method == 0) return rgba; 

 else if (output_conversion_method == 1) return linear2sRGB(rgba); 

 else return sRGB2linear(rgba); 

}
```


## 抖动

这些是向着色器添加抖动的一些帮助程序。

使用8x8 Bayer矩阵进行抖动模式

```
import lib-bayer.glsl 

 

float getDitherThreshold(uvec2 coords) 

{ 

  return bayerMatrix8(coords); 

} 

 

 

vec4 RGB2Gray(vec4 rgba) 

{ 

  float gray = 0.299 * rgba.r + 0.587 * rgba.g + 0.114 * rgba.b; 

  return vec4(vec3(gray), rgba.a); 

}
```


移除光滑金属表面（接近镜像）上的AO和阴影

```
float specularOcclusionCorrection(float diffuseOcclusion, float metallic, float roughness) 

{ 

  return mix(diffuseOcclusion, 1.0, metallic * (1.0 - roughness) * (1.0 - roughness)); 

} 

 
```
