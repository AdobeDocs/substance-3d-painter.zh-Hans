---
breadcrumb-title: ""
description: 访问Substance 3D Painter的Lib Bayer着色器 API参考，在自定义着色器中创建Bayer仿色图案。
title: Lib Bayer -着色器 API
user-guide-description: ""
user-guide-title: ""
source-git-commit: 6b6d52207ca1d043aaa1b2b14145b6b49d4c1942
workflow-type: tm+mt
source-wordcount: '32'
ht-degree: 0%
---

# Lib Bayer -着色器 API

## lib-bayer.glsl

**公共函数：** *bayerMatrix8*

```
float bayerMatrix8(uvec2 coords) { 

  return (float(bayer(coords.x, coords.y)) + 0.5) / 64.0; 

} 

 
```
