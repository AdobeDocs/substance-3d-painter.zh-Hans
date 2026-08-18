---
title: Lens-flare
description: ''
helpx_description: "Substance 3D Painter"
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/features/post-processing/lens-flare.html"
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 7%

---


# 镜头光晕

![](../../assets/v12_post_flare.jpg)

模拟明亮光源与相机镜头元素相互作用时产生的光学伪影，从而创建光晕、条纹和虚影反射。

| <b>参数</b> | <b>描述</b> |
| --- | --- |
| <b>分辨率</b> | 设置镜头光晕效果的内部渲染分辨率。 值越高，条纹越锐利，但可能会影响性能。 |
| <b>相机</b> | 选择用于模拟光晕的摄像机模型。 可能的值为：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>全景镜头</b>（较短的焦距） </li> <li data-preserve-html="true"><b>长焦镜头</b>（较长的焦距）。</li> </ul> |
| <b>金额</b> | 控制光晕效果的整体强度。 该值可以超过1.0以增加强度。 |
| <b>阈值</b> | 确定生成光晕所需的最小图像明度。 值越低，产生光晕的区域越多，而值越高，对非常明亮的光源产生的效果就越有限。 |
| <b>光圈缩放</b> | 缩放用于光晕计算的孔径形状的大小，影响光晕元素的整体大小。 |
| <b>涂层厚度</b> | 模拟镜头元件上的抗反射涂层。 涂层Thickness会影响光线的散点，从而改变光晕的颜色。 |
| <b>涂层IOR</b> | 模拟镜头的折射率：光线通过其Thickness的方式。 值越低，产生的鬼影越集中。 |
| <b>遮蔽缩放</b> | 设置受影响中心区域的尺寸。 |
| <b>Smoothness</b> | 控制镜头光晕的渐隐程度。 值越高，过渡越柔和。 |
| <b>唯一的重影</b> | 定义光晕形状的变化程度。 较高的值可能会显着影响性能。 |
| <b>虚影位置缩放</b> | 控制光斑重影的扩散范围和尺寸。 |
| <b>光圈纹理</b> | 定义用于生成光晕图案的镜头光圈的形状。 纹理控制衍射和虚影形状。 |
