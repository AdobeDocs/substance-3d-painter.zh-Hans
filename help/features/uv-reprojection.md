---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/features/uv-reprojection.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中使用UV重投影，在不同的UV布局之间转移纹理。
helpx_creative_field: ""
helpx_description: Painter > Features > UV Reprojection
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: UV重投影
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 0%

---


# UV重投影

UV重新投影是一个自动过程，在更改纹理分辨率或导入新网格时发生。\
如果在文档中加载新网格（通过[项目配置](https://substance3d.adobe.com/display/draftpainter/project%20configuration)窗口），则所有操作都将重新投影到该新网格上。 拓扑是否更改（只要相似）或UV是否更改并不重要。 由于重新投影是通过重新计算所有图层和画笔描边进行的，因此可能需要一些时间（特别是在高纹理分辨率的情况下）。

在2D视图中绘画

由于在2D视图中进行的每个描边都是在UV空间中执行的，因此如果重新导入后网格的UV发生剧烈变化，则无法正确重新投影该描边。 制作项目重新投影校样的最佳方法是依赖ID地图和其他类型的选择和绘画的蒙版而不是3D视图。

## 重新投影是如何工作的？

Substance 3D Painter将其数据以3D形式保存在世界空间中，以保持所有内容无损。 这意味着，重新导入网格时，Substance 3D Painter会尝试在重新导入之前网格的位置绘制，但无法知道某些部分可能移动到哪里。

此外，Substance 3D Painter导入网格时，会计算其定界框以注册空间并定义工具（画笔、粒子等）的相对缩放。 此边框在每个轴上有1个单位的宽度。 导入新网格时，如果取消选中“保留描边”，则我们将边界框重新标准化为新网格。 因此，如果网格的大小发生了显着变化，描边也会移动。 但是，如果选中“保留描边”，则我们会将原始定界框缩放为新定界框，以便正确重新投影画笔描边。

>[!WARNING]
>
> 更改3D网格的单位可能会导致UV重新投影不起作用；即使拓扑没有更改，旧网格和新网格也可解释为截然不同的缩放。 理想情况下，应避免更改设备设置，因为这可能很难修复。
