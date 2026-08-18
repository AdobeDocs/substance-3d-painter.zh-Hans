---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/scripting-and-development/api-reference/shader-api/parameters-shader-api/layering-declare-stacks-shader-api.html"
breadcrumb-title: ''
description: 访问Substance 3D Painter的“图层声明栈叠”着色器 API参考以创建自定义素材图层栈叠。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > API Reference > Shader API > Parameters - Shader API > Layering Declare Stacks - Shader API
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 分层声明栈栈 — 着色器 API
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# 分层声明栈栈 — 着色器 API

## 材质图层：声明可编辑的栈叠

可编辑栈栈由唯一标识符和文档通道列表定义。 可能的通道ID为： *ambientocclusion* *各向异性* *各向异性* *基色* *blendingmask* *扩散* *位移* *发射* *光泽度* *Height* *i或* *金属* *正常&lbrace;25*&#x200B;不透明度&#x200B;**&#x200B;反射&#x200B;**&#x200B;粗糙度&#x200B;**&#x200B;散射&#x200B;** Specular **&#x200B;反射级&#x200B;**&#x200B;传输&#x200B;**&#x200B;用户0 &#x200B;**&#x200B;用户1 **&#x200B;用户2 &#x200B;**&#x200B;用户3 **&#x200B;用户4 &#x200B;**&#x200B;用户5 **&#x200B;用户6 &#x200B;**&#x200B;用户7 **

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


要将栈栈中的通道绑定到取样器参数，请在通道标记前面添加栈栈标识符：

```
//: param auto Mask1.channel_opacity 

uniform sampler2D mask_tex1; 

//: param auto Mask2.channel_opacity 

uniform sampler2D mask_tex2; 

 
```
