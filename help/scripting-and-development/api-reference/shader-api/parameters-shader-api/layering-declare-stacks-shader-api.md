---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/scripting-and-development/api-reference/shader-api/parameters-shader-api/layering-declare-stacks-shader-api.html"
breadcrumb-title: ''
description: 访问Substance 3D Painter的图层声明堆叠着色器 API参考以创建自定义材料图层堆叠。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > API Reference > Shader API > Parameters - Shader API > Layering Declare Stacks - Shader API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 分层声明堆叠-着色器 API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# 分层声明堆叠-着色器 API

## 材料分层：声明可编辑的堆叠

可编辑的堆叠由唯一的标识符和文档通道列表定义。 可能的通道ID为： *ambientocclusion* *各向异性角度* *各向异性层级* *基色* *blendingmask* *扩散* *位移* *emissive* *光泽度* *Height* *或* *金属* *正常* *不透明度* *反射* *粗糙度* *散射* *Specular* *规范级别* *transmissive* *用户0* *用户1* *用户2* *用户3* *用户4* *用户5* *用户6* *用户7*

示例：

```
//:  stacks [ 

//:    { 

//:      "id": "Mask1", 

//:      "channels": [ 

//:        {"id": "opacity"} 

//:      ] 

//:    }, { 

//:      "id": "Mask2", 

//:      "channels": [ 

//:        {"id": "opacity"}, 

//:        {"id": "user0"} 

//:      ] 

//:    } 

//:  ]
```


要将通道从堆叠绑定到取样器参数，请在通道标记前面加上堆叠标识符：

```
//: param auto Mask1.channel_opacity 

uniform sampler2D mask_tex1; 

//: param auto Mask2.channel_opacity 

uniform sampler2D mask_tex2; 

 
```
