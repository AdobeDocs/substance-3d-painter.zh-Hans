---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/scripting-and-development/api-reference/shader-api/parameters-shader-api/all-engine-params-shader-api.html"
breadcrumb-title: ''
description: 访问Substance 3D Painter的“所有引擎参数”着色器 API参考，以控制引擎级着色器参数。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > API Reference > Shader API > Parameters - Shader API > All Engine Params - Shader API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 所有引擎参数 — 着色器 API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---


# 所有引擎参数 — 着色器 API

## 引擎参数示例

## 纹理参数

Substance Painter使用稀疏虚拟纹理(SVT)系统在视区中显示纹理。

有关此系统的详细信息，请转到[联机文档](../../../../features/sparse-virtual-textures.md)。

此系统对着色器代码的编写有影响。 我们提供了帮助程序以通过&#x200B;*SamplerSparse*&#x200B;结构和纹理查找函数来简化其使用（请参阅[lib-sparse.glsl](../libraries-shader-api/lib-sparse-shader-api.md)）。

基本用法：

```
// Defines the SamplerSparse structure 

import lib-sparse.glsl 

 

//: param auto TEXTURE_TAG 

uniform SamplerSparse uniform_tex;   // Texture sampler and its information
```


纹理参数允许使用“or”运算符定义回退：

```
//: param auto TEXTURE_TAG_1 or TEXTURE_TAG_2 

uniform SamplerSparse uniform_tex; // if TEXTURE_TAG_1 exists then TEXTURE_TAG_1 else TEXTURE_TAG_2
```


其中&#x200B;*TEXTURE\_TAG*&#x200B;是下面描述的标记之一。

### 文档的通道标记

所有这些纹理都是&#x200B;**预乘**&#x200B;和&#x200B;**扩展**&#x200B;的，以避免接缝问题。

**纹理集通道**

*channel\_ambientocclusion* *channel\_anisotropyangle* *channel\_anisotropylevel* *channel\_basecolor* *channel\_blendingmask* *channel\_sponal* *channel\_位移* *channel\_emissive* *channel\_glssiness* *channel\_Height* *channel\_ior* *channel\_metallic* *channel\_normal* *channel\_opacity* *channel\_reflection* *channel\_roughness* *channel\_sparteration* *channel\_specularlevel* *channel\_transmissive***

**用户渠道**

*channel\_user0* *channel\_user1* *channel\_user2* *channel\_user3* *channel\_user4* *channel\_user5* *channel\_user6* *channel\_user7*

### 网格图

*texture\_ambientocclusion* ：环境遮蔽映射\
*纹理\_曲率* ：曲率图\
*纹理\_id* ： ID映射\
*纹理\_normal* ：正切空间法线映射\
*纹理\_normal\_ws* ：世界空间法线图\
*纹理\_位置* ：世界空间位置地图\
*纹理\_Thickness* ：Thickness映射

## 其他纹理参数

基本用法：

```
//: param auto TEXTURE_TAG 

uniform sampler2D uniform_tex;   // The texture itself 

 

//: param auto TEXTURE_TAG_size 

uniform vec4 uniform_tex_size;   // The size of the texture (width, height, 1/width, 1/height)
```


纹理参数允许使用“or”运算符定义回退：

```
//: param auto TEXTURE_TAG_1 or TEXTURE_TAG_2 

uniform sampler2D uniform_tex; // if TEXTURE_TAG_1 exists then TEXTURE_TAG_1 else TEXTURE_TAG_2 

 

//: param auto TEX_TAG_1_size or TEX_TAG_2_size 

uniform vec4 uniform_tex_size; // if TEX_TAG_1 exists then TEX_TAG_1_size else TEX_TAG_2_size
```


其中&#x200B;*TEXTURE\_TAG*&#x200B;是下面描述的标记之一。

*纹理\_blue\_noise* ：蓝色杂色纹理\
*texture\_environment* ：环境映射，**mip映射**，使用[lib-env.glsl](../libraries-shader-api/lib-env-shader-api.md)来使用此映射

## 其他参数

*长宽比* ：包含视口&#x200B;*宽度/Height*&#x200B;比值的&#x200B;*浮点*

```
//: param auto aspect_ratio 

uniform float uniform_aspect_ratio;
```


*camera\_view\_matrix* ：表示从世界空间到相机空间转换的&#x200B;*mat4*

```
//: param auto camera_view_matrix 

uniform mat4 uniform_camera_view_matrix;
```


*camera\_view\_matrix\_it* ：*camera\_view\_matrix*&#x200B;的反转置版本

```
//: param auto camera_view_matrix_it 

uniform mat4 uniform_camera_view_matrix_it;
```


*camera\_vp\_matrix\_inverse* ： *投影\* camera\_view\_matrix*矩阵的逆矩阵

```
//: param auto camera_vp_matrix_inverse 

uniform mat4 uniform_camera_vp_matrix_inverse;
```


*环境\_曝光* ：表示envmap曝光的&#x200B;*浮点*

```
//: param auto environment_exposure 

uniform float uniform_environment_exposure;
```


*environment\_max\_lod* ：表示mip映射金字塔的envmap深度的&#x200B;*float*

```
//: param auto environment_max_lod 

uniform float uniform_max_lod;
```


*环境\_旋转* ：表示环境映射绕上轴旋转的&#x200B;*浮点*\
该值在范围[0,1]内，应映射到范围[0， 2\*pi]

```
//: param auto environment_rotation 

uniform float uniform_environment_rotation;
```


*面* ：一个指示已渲染面（–1：后面，0：未定义，1：前面）的&#x200B;*整数*\
值为0意味着您可以安全地依赖glsl内置变量&#x200B;*gl\_FrontFacing*

```
//: param auto facing 

uniform int uniform_facing;
```


*fovy* ：表示沿Y轴的相机视场的&#x200B;*浮点*

```
//: param auto fovy 

uniform float uniform_fovy;
```


*is\_2d\_view* ：一个&#x200B;*bool*，指示是否为2D视图执行渲染

```
//: param auto is_2d_view 

uniform bool uniform_2d_view;
```


*is\_perspective\_projection* ：指示投影是透视投影还是正交投影的&#x200B;*bool*

```
//: param auto is_perspective_projection 

uniform bool uniform_perspective_projection;
```


*main\_light* ：表示环境中主光位置的&#x200B;*vec4*

```
//: param auto main_light 

uniform vec4 uniform_main_light;
```


*mvp\_matrix* ：表示模型视图投影矩阵的&#x200B;*mat4*

```
//: param auto mvp_matrix 

uniform mat4 uniform_mvp_matrix;
```


*scene\_original\_radius* ： *浮点*，表示场景定界球在规范化前的半径

```
//: param auto scene_original_radius 

uniform float uniform_scene_original_radius;
```


*screen\_size* ：包含屏幕大小数据&#x200B;*（宽度、Height、1/宽度、1/Height）的* vec4 **

```
//: param auto screen_size 

uniform vec4 uniform_screen_size;
```


*world\_camera\_direction* ：表示世界相机方向的&#x200B;*vec3*

```
//: param auto world_camera_direction 

uniform vec3 uniform_world_camera_direction;
```


*world\_eye\_position* ：表示世界眼睛位置的&#x200B;*vec3*

```
//: param auto world_eye_position 

uniform vec3 uniform_world_eye_position; 

 
```
