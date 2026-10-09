---
breadcrumb-title: ""
description: 访问Substance 3D Painter的LibEmissive着色器 API参考，以创建emissive材料和发光效果。
title: 库Emissive-着色器 API
user-guide-description: ""
user-guide-title: ""
source-git-commit: 6b6d52207ca1d043aaa1b2b14145b6b49d4c1942
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 0%
---

# 库Emissive-着色器 API

## lib-emissive.glsl

**公共函数：** *pbrComputeEmissive*

从库导入

```
import lib-sparse.glsl
```


emissive声道纹理。

```
//: param auto channel_emissive 

uniform SamplerSparse emissive_tex;
```


用于微调emissive强度的值。

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


计算观看者眼睛的emissive亮度

```
vec3 pbrComputeEmissive(SamplerSparse emissive, SparseCoord coord) 

{ 

  return emissive_intensity * textureSparse(emissive, coord).rgb; 

} 

 
```
