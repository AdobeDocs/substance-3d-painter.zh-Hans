---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/scripting-and-development/api-reference/shader-api/shaders-shader-api/surface-shader-shader-api.html"
breadcrumb-title: ''
description: 访问Substance 3D Painter的“表面”着色器 API参考，以创建自定义表面着色器效果和材质。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > API Reference > Shader API > Shaders - Shader API > Surface Shader - Shader API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 表面着色器 — 着色器 API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

---


# 表面着色器 — 着色器 API

## surface-shader.glsl

要创建可用于Substance Painter的着色器资源，只需创建一个包含以下配置文件且包含一个名为&#x200B;*shade*&#x200B;函数的glsl文件：

```
void shade(V2F inputs);
```


## V2F输入类型定义：

```
struct V2F { 

  vec3 normal;               // interpolated normal 

  vec3 tangent;              // interpolated tangent 

  vec3 bitangent;            // interpolated bitangent 

  vec3 position;             // interpolated position 

  vec4 color[1];             // interpolated vertex colors (color0) 

  vec2 tex_coord;            // interpolated texture coordinates (uv0) 

  SparseCoord sparse_coord;  // interpolated sparse texture coordinates used by textureSparse() sampling function 

  vec2 multi_tex_coord[8];   // interpolated texture coordinates (uv0-uv7) 

};
```


注意：要获取uv1-uv7的SparseCoord，必须显式调用[lib-sparse.glsl](../libraries-shader-api/lib-sparse-shader-api.md)中定义的&#x200B;*getSparseCoord(vec2)*

## 曲面着色器输出：

可以从&#x200B;*shade*&#x200B;函数内部调用以下函数来说明片段属性：

```
// fragment opacity. default value: 1.0 

void alphaOutput(float); 

// diffuse lighting contribution. default value: vec3(0.0) 

void diffuseShadingOutput(vec3); 

// specular lighting contribution. default value: vec3(0.0) 

void specularShadingOutput(vec3); 

// color emitted by the fragment. default value: vec3(0.0) 

void emissiveColorOutput(vec3); 

// fragment color. default value: vec3(1.0) 

void albedoOutput(vec3); 

// subsurface scattering properties, see lib-sss.glsl for details. default value: vec4(0.0) 

void sssCoefficientsOutput(vec4);
```


例如，用于计算碎片颜色的最基本渲染方程为： *emissiveColor +反照率\* spinderShading +镜面底纹*
