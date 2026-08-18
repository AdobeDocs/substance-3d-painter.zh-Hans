---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/scripting-and-development/api-reference/shader-api/parameters-shader-api/all-rendering-states-params-shader-api.html"
breadcrumb-title: ''
description: 访问Substance 3D Painter的“所有渲染状态参数”着色器 API参考，以控制渲染状态参数。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > API Reference > Shader API > Parameters - Shader API > All Rendering States Params - Shader API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 所有渲染状态参数 — 着色器 API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 2%

---


# 所有渲染状态参数 — 着色器 API

## 渲染状态示例

## 背面消隐

去除背面：

```
//: state cull_face on
```


绘制正面和背面：

```
//: state cull_face off
```


## 混合

无混合、完全不透明的对象：

```
//: state blend none
```


前后绘制顺序的标准混合模式：

```
//: state blend over
```


前后绘制顺序的标准混合模式。 假定颜色已预先乘以Alpha：

```
//: state blend over_premult
```


叠加混合模式：

```
//: state blend add
```


乘法混合模式：

```
//: state blend multiply
```


## 着色器取样区域

默认情况下，使用未变换的纹理坐标对文档通道进行采样，以便在绘画过程中进行渲染优化。

如果出现伪像，请将&#x200B;*非本地*&#x200B;状态设置为&#x200B;*上的* 。

```
//: state nonlocal on 

 
```
