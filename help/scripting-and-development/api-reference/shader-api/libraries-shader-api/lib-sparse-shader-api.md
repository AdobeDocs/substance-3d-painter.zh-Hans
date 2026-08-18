---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/scripting-and-development/api-reference/shader-api/libraries-shader-api/lib-sparse-shader-api.html"
breadcrumb-title: ''
description: 访问Substance 3D Painter的Lib稀疏着色器 API参考，以便在自定义着色器中使用稀疏纹理采样。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > API Reference > Shader API > Libraries - Shader API > Lib Sparse - Shader API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 库稀疏 — 着色器 API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---


# 库稀疏 — 着色器 API

## lib-sparse.glsl

此文件提供有助于确保稀疏纹理采样正确性(ARB\_sparse\_texture)的功能。 仅对视频内存中真实存在的部分纹理进行取样。

**公共函数：** *getSparseCoord* *getSparseCoordLod0* *textureSparseQueryLod* *textureSparse*

**公共结构：** *SamplerSparse* *稀疏代码*

仅在启用了稀疏虚拟纹理扩展时定义&#x200B;*FEATURE\_SPARSE\_TEXTURE*&#x200B;宏。

如果启用，请处理其他纹理查找检查，以便在缺少纹理时向上爬过mipmap金字塔。

```
## ifdef FEATURE_SPARSE_TEXTURE

//: param auto material_lod_check_needed 

uniform bool material_lod_check_needed = false; 

//: param auto material_lod_mask 

uniform usampler2D material_lod_mask; 

## endif // FEATURE_SPARSE_TEXTURE

//: param auto uvtile_reference_sampler 

uniform sampler2D uvtile_reference_sampler; 

//: param auto uvtile_size 

uniform vec2 uvtile_size; 

//: param auto uvtile_inverse_size 

uniform vec2 uvtile_inverse_size; 

//: param auto uvtile_lod_bias 

uniform float uvtile_lod_bias;
```


Sampler和稀疏纹理信息结构

用于通过单个自动绑定查询所有与Sampler相关的制服

```
struct SamplerSparse { 

  sampler2D tex; 

  vec4 size; // width, height, 1/width, 1/height 

  bool is_set; // a boolean indicating whether the texture is in the texture set or not 

  uvec3 lod_mask_select; // masking operations description allowing to retrieve loaded mipmaps information 

};
```


稀疏采样坐标

存储UV坐标和材料级稀疏LoD蒙版

```
struct SparseCoord { 

  vec2 tex_coord; 

  vec2 dfdx; 

  vec2 dfdy; 

  float lod; 

  uint material_lod_mask; 

}; 

 

 

## if defined(SHADER_FRAGMENT)
```


生成&#x200B;*textureSparse()*&#x200B;采样函数使用的纹理坐标结构（必须从片段着色器调用）

示例： *SparseCoord uv1coord = getSparseCoord(inputs.multi\_tex\_coord[1])；*

```
SparseCoord getSparseCoord(vec2 tex_coord) { 

  SparseCoord res; 

  res.tex_coord = tex_coord; 

  res.dfdx = dFdx(tex_coord); 

  res.dfdy = dFdy(tex_coord); 

## ifdef FEATURE_SPARSE_TEXTURE

  res.material_lod_mask = material_lod_check_needed ? 

    textureLod(material_lod_mask,tex_coord,0.0).r : 

    0u; 

  res.lod = getLodFromReferenceSampler(tex_coord); 

## endif // FEATURE_SPARSE_TEXTURE

  return res; 

} 

## endif
```


生成&#x200B;*textureSparse()*&#x200B;采样函数使用的纹理坐标结构基级别采样版本（如果位于片断着色器外部，则可以使用）

```
SparseCoord getSparseCoordLod0(vec2 tex_coord) { 

  SparseCoord res; 

  res.tex_coord = tex_coord; 

  res.dfdx = vec2(0.0); 

  res.dfdy = vec2(0.0); 

## ifdef FEATURE_SPARSE_TEXTURE

  res.material_lod_mask = material_lod_check_needed ? 

    textureLod(material_lod_mask,tex_coord,0.0).r : 

    0u; 

  res.lod = 0.0; 

## endif // FEATURE_SPARSE_TEXTURE

  return res; 

} 

 

## if defined(SHADER_FRAGMENT)
```


计算用于从稀疏纹理中采样的细节级别

如果纹理缺失，向上爬过mipmap金字塔返回LoD BEFORE LoD bias applied

```
float textureSparseQueryLod(SamplerSparse sampler, SparseCoord coord) { 

## ifdef FEATURE_SPARSE_TEXTURE

  float lodfix = coord.lod; 

  if (material_lod_check_needed) { 

    lodfix = getFixedSparseLod(getTextureLodMask(sampler.lod_mask_select, coord.material_lod_mask), lodfix); 

  } 

  return lodfix-uvtile_lod_bias; 

## else // FEATURE_SPARSE_TEXTURE

  return textureQueryLod(sampler.tex, coord.tex_coord).y-uvtile_lod_bias; 

## endif // FEATURE_SPARSE_TEXTURE

} 

## endif // SHADER_FRAGMENT
```


计算用于从稀疏纹理中采样的导数

如果缺少纹理，请向上爬过mipmap金字塔

```
void textureSparseQueryGrad(out vec2 dfdx, out vec2 dfdy, SamplerSparse sampler, SparseCoord coord) { 

## ifdef FEATURE_SPARSE_TEXTURE

  if (material_lod_check_needed) { 

    float lodfix = getFixedSparseLod(getTextureLodMask(sampler.lod_mask_select, coord.material_lod_mask), coord.lod); 

    if (coord.lod!=lodfix) { 

      // Fix dfdx dfdy, take account offset, no more anisotropy 

      vec2 ddfix = exp2(lodfix-uvtile_lod_bias) * uvtile_inverse_size; 

      dfdx = vec2(ddfix.x,0.0); 

      dfdy = vec2(0.0,ddfix.y); 

      return; 

    } 

  } 

## endif // FEATURE_SPARSE_TEXTURE

  dfdx = coord.dfdx; 

  dfdy = coord.dfdy; 

}
```


在稀疏纹理上执行纹理查找，必要时向上查找多级渐远纹理级别

此函数替代标准&#x200B;*纹理(sampler2D， vec2)*&#x200B;以从稀疏纹理检索纹理元素

```
vec4 textureSparse(SamplerSparse sampler, SparseCoord coord) { 

  vec2 dfdx,dfdy; 

  textureSparseQueryGrad(dfdx, dfdy, sampler, coord); 

  return textureGrad(sampler.tex, coord.tex_coord, dfdx, dfdy); 

}
```


给定纹理，使用小偏移执行优化的多纹理查找

我们提供此帮助程序的替代版本，最多N=4

```
void textureSparseOffsets(SamplerSparse sampler, SparseCoord coord, vec2 offsets[N], out vec4 results[N]) { 

  vec2 dfdx,dfdy; 

  textureSparseQueryGrad(dfdx, dfdy, sampler, coord); 

  for(int i = 0; i < N; ++i) { 

    results[i] = textureGrad(sampler.tex, coord.tex_coord + offsets[i], dfdx, dfdy); 

  } 

} 

 
```
