---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/painting/tool-list/clone-tool.html"
breadcrumb-title: ''
description: 使用Substance 3D Painter中的仿制工具将纹理细节从一个区域复制到另一个区域，以实现无缝的纹理绘画。
helpx_creative_field: ""
helpx_description: Painter > Painting > Tool list > Clone Tool
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Clone Tool
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 1%

---


# Clone Tool

在Substance 3D Painter 2中引入后，仿制工具与[绘画工具](https://support.allegorithmic.com/documentation/display/SPDOC/Paint+brush)共享相同类型的参数。 顾名思义，仿制工具允许您从一点到另一点复制特定图层或完整图层栈栈的内容。

![](../../assets/clone-01.gif)

## 使用情况

使用仿制工具的最简单的方法就是对绘画图层的内容使用该工具。

这可以通过两个步骤来完成：

* 将鼠标放在模型上并按“**V**”键，选择源位置。
* 然后将鼠标放在重复区域出现的位置并开始绘画。

可以随时通过再次按“**V**”来更新源。

![](../../assets/2018-06-12-18-11-59.png)

默认情况下，在使用“仿制”工具绘画时，源位置将遵循，并在画笔释放后更新其位置。 通过禁用用于“**仿制源行为**”的按钮，源将返回到按“**V**”时定义它的位置。 在使用相同的源区域多次绘制时，此功能非常有用。

使用仿制工具的一种更智能的方法是创建绘画图层，并将所有通道的混合模式设置为“穿透”。 这样，就可以从“仿制图层”下方的所有图层以非破坏性方式复制任何信息。 下面的图层将保持不变，而仿制图层将考虑稍后应用的任何修改：

![](../../assets/clone-02.gif)
