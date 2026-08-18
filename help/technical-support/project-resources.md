---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/project-resources.html"
breadcrumb-title: ''
description: 访问Substance 3D Painter的项目资源和技术文档，以改进您的工作流程和疑难解答。
helpx_creative_field: ""
helpx_description: Substance 3D Painter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 项目资源
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---


# 项目资源和设置

在Painter中，管理项目资源有助于为您的项目性能奠定良好的基础。

+++缩放已烘焙贴图
有时，并非所有已烘焙贴图都需要达到2k或4k分辨率。 毫不犹豫地在2k温度下烘焙一批，然后在较低分辨率下重烤，看看是否存在视觉差异。

+++

+++管理导入的位图
导入的图像可能会严重影响性能，因此务必要注意导入的内容。 如果纹理集设置为2k，并且无论如何都不会以更高的分辨率导出，则使用8k图像不会产生任何正面影响 — 其质量将限制为2k，因为它是纹理集的分辨率。

排版也很重要 — EXR、HDR甚至PNG比JPG重得多，而且并非所有图像都需要EXR的品质级别（例如，基色与Height细节）。

+++

+++调整着色器设置
Ultra的Specular质量将给出更准确的结果，但设置成本很高。 着色器中一次启用的效果越多，计算就越大。 如有可能，请使用单独的着色器将复杂素材拆分为另一个纹理集。 如果启用了位移，请谨慎使用tessellation参数。

+++

+++调整文件选项
使用<b>“文件”>“存储”>“存储并缩减文件”</b> <b>大小为</b>以刷新不需要的数据，并使用<b>删除未使用的资源</b>来消除导入到项目中但项目内任何位置未使用的文件。

+++
