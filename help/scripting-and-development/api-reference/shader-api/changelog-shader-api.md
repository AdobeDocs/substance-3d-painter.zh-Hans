---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/scripting-and-development/api-reference/shader-api/changelog-shader-api.html"
breadcrumb-title: ''
description: 查看着色器 API的更改日志，以跟踪随时间推移的更新、新功能和更改。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > API Reference > Shader API > Changelog - Shader API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 更改日志 — 着色器 API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 3%

---


# 更改日志 — 着色器 API

## 更改日志

## 2018.3.2

* [lib-sparse.glsl](libraries-shader-api/lib-sparse-shader-api.md)：采样函数使用纹理导数代替简单多级渐远纹理级别。 这是对各向异性采样的支持要求。 采样函数签名不会被修改。
* [lib-pom.glsl](libraries-shader-api/lib-pom-shader-api.md)： *getParallaxOffset*&#x200B;函数签名已更改，以使用纹理衍生产品

## 2018.3.0

* 添加新的[lib-pbr-aniso.glsl](libraries-shader-api/lib-pbr-aniso-shader-api.md)库以帮助可视化各向异性Specular高光
* 添加新的[lib-sparse.glsl](libraries-shader-api/lib-sparse-shader-api.md)库，通过确保mipmaps的可用性来帮助进行通道采样
* 更新着色器库界面以完成此安全取样
* **弃用**：先前基于vec2纹理坐标和纹理取样器的函数已被弃用（请使用新签名）
* [lib-pom.glsl](libraries-shader-api/lib-pom-shader-api.md)：添加&#x200B;*applyParallaxOffset*&#x200B;函数以简化视差遮蔽效果的使用
* [lib-random.glsl](libraries-shader-api/lib-random-shader-api.md)：添加蓝色噪声随机值生成器和时间替代项
* [lib-sampler.glsl](libraries-shader-api/lib-sampler-shader-api.md)：拆分所有通道采样帮助程序以同时具有值解释和采样帮助程序

## 2018.2.0

* **表面着色器 API更改**： *shade*&#x200B;函数签名已更改，请参阅[surface-shader.glsl](shaders-shader-api/surface-shader-shader-api.md)
* *shadeShadow*&#x200B;函数不再使用，可以安全地从自定义表面着色器中移除
* 添加次表面散射支持，请参阅[surface-shader.glsl](shaders-shader-api/surface-shader-shader-api.md)和[lib-sss.glsl](libraries-shader-api/lib-sss-shader-api.md)以获取详细信息
* [lib-pbr.glsl](libraries-shader-api/lib-pbr-shader-api.md)： *pbrComputeBRDF*&#x200B;函数已被删除。 请参阅[pbr-metal-rough.glsl](shaders-shader-api/pbr-metal-rough-shader-api.md)示例，立即了解如何使用库
* 已添加新引擎参数： *纹理\_blue\_noise*、*长宽比*、*camera\_vp\_matrix\_inverse*、*环境\_曝光*、*环境\_旋转*、*fovy*、*main\_light*&#x200B;和&#x200B;*screen\_size*。 有关详细信息，请参阅[all-engine-params.glsl](parameters-shader-api/all-engine-params-shader-api.md)
* 添加&#x200B;*描述*&#x200B;元数据以提供自定义着色器参数的工具提示

## 2017.4.2

* 修复文档示例中缺少的着色器（像素化和卡通着色器）
* 修复抖动以获取高分辨率
  * [lib-bayer.glsl](libraries-shader-api/lib-bayer-shader-api.md)： **bayerMatrix8()**&#x200B;返回> 4k坐标的有效值

## 2017.4.1

* 固定PBR涂层着色器
  * [lib-vector.glsl](libraries-shader-api/lib-vectors-shader-api.md)： **tangentSpaceToWorldSpace()**&#x200B;和&#x200B;**worldSpaceToTangentSpace()**&#x200B;输出现在已规范化

## 2017.4.0

* 某些网格在2D视图中的Specular反射不正确

## 2017.3.1

* 更便宜的抖动

## 2017.2.0

* 移除插值tbn标准化以匹配Substance Designer和面包师行为
* [视港]用斐波那契螺旋代替哈默斯利桌子

## 2.6.0

* 修复着色器混合和剔除模式
* 重做抖动。 现在，如果我们有一个线性渲染，我们将其应用于颜色配置文件

## 2.5.0

* 在视区中添加对颜色配置文件(LUT)的支持（可选sRGB转换）
* 向着色器中的不透明度添加抖动
* 将视差遮蔽映射添加到PBR着色器
* 添加在默认着色器UI中隐藏自定义参数的方法
* 在图层着色器文档中添加指向通道标记列表的链接
* 将“channel\_ao”标记替换为“channel\_ambientocclusion”
* [视区]某些正常映射具有固定值，这些值显示为伪像
* 修复着色器文档中的可用通道
* 允许定义自定义着色器UI
* 为材质图层着色器添加标准的自定义着色器UI
* 自定义UI文件现在相对于书架中的着色器/自定义UI文件夹（如mdl）进行搜索
* 在默认着色器中使用Specular level通道
* 修复vec3着色器参数示例
* 将Painter升级到OpenGL核心配置文件

## 2.4.0

* 修复合并导出的法线图与视区中显示的法线图之间的差异

## 2.2.0

* 在非文档纹理的通用素材中添加对无绑定纹理的支持
* 更新自定义着色器滑块文档
* 允许定义滑块的步长精度
* 动态材质分层文档

## 2.1.1

* 在lib-utils中添加“RGB2Gray”函数

## 2.1.0

* 允许为着色器参数和材质/蒙版定义组
* 在文档中添加缺失的通道(“ao”、“spinder”、“specularlevel”)

## 2.0.4

* 使用低Alpha值的正常解包函数不正确
* 允许在自定义着色器中读取网格顶点颜色
* [视口]某些计算机上的延长环境映射

## 2.0.0

* 允许按专用通道覆盖普通/AO附加映射
* 将Height2Normal函数更改为使用Sobel方法
* 添加为每个着色器定义模型的可能性
* 在架子中添加新的mdl文件夹
* 添加扩散和Specular level通道预设
* 色调映射的文档更新
* 在正交模式下修复反射
* 修复了环境图上特定位置出现的垂直白色毛刺
* 允许为纹理参数定义“default\_color”

## 1.7.0

* 允许从货架上取样外部纹理

## 1.6.0

* 显示灰度系数/色调映射功能以允许覆盖它们
* 公开多个文本代码

## 1.5.0

* 在着色器错误报告中添加行号和文件名

## 1.4.1

* 所有sRGB转换均遵循sRGB标准，但具有近似值的着色器除外
* 将Height通道转换为法线映射，导致色彩空间错误

## 1.4.0

* 添加环境遮蔽通道
* 为普通版本添加新工作流
* 为与纹理相关的自动参数添加“or”表达式语法
* 在OSX上修复Intel gpu的pbr着色器

## 1.3.4

* 允许在片段着色器中插入二项式
* 固定Mikt切线空间

## 1.3.3

* 产生负光强度的固定球面谐波
* 曝光度计算与Substance Designer（并修复曝光度滑块）不同
* 100%金属表面上不应出现阴影

## 1.3.0

* 添加阴影函数
* 添加对不透明度（“alpha\_test”和“alpha\_blend”）的支持

## 1.2.0

* 能够将所需的openGL状态设置为自定义着色器
* 修复反相噪点
* 添加对普通渠道的支持

## 1.0

* 添加对自定义着色器的支持
