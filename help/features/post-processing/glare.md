---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/features/post-processing/glare.html"
breadcrumb-title: ''
description: 了解如何使用Substance 3D Painter中的眩光后期处理效果为明亮区域添加镜头眩光和开花效果。
helpx_creative_field: ""
helpx_description: Painter > Features > Post Processing > Glare
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Glare
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 1%

---


# Glare

![](../../assets/glare-example.jpg)![](../../assets/glare.png)

参数说明：

| 设置 | 描述 |
| --- | --- |
| **明亮度** | 这是眩光效果的整体亮度。 将此值设置为0.0会完全禁用该效果。  实际值出现在约0.5到4.0的范围内，最大值为16.0。 |
| **阈值** | 仅提取比阈值亮的像素以生成眩光。  对于自然效果，建议使用介于0.0和1.0之间的值。 |
| **重新映射** **因子** | 指定除1.0以外的值导致所提取的高明亮度分量被进一步非线性扩展（或压缩）。 如果传递大于1.0的值，则明亮像素的眩光将变得更强。  使用此选项可单独调整眩光的明亮度映射，而不会影响其他效果。 明亮传递后的明亮度在平滑曲线中增加，明亮度值1.0接近&#x200B;**重映射因数**，大于1.0的值接近（**重映射** **因数** ^2）。 |
| **形状** | 形状定义了眩光的外观，提供了不同的模型：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>开花</strong> ：仅开花效果。</li><li data-preserve-html="true"><strong>镜头眩光：</strong>开花/幽灵(镜头眩光)/余影。</li><li data-preserve-html="true"><strong>标准：</strong>类型包括所有基本元素的良好平衡。</li><li data-preserve-html="true"><strong>便宜镜头：</strong>廉价镜头的尖锐重影和其他表现形式。 </li><li data-preserve-html="true"><strong>图像之后：</strong>具有非常强残影的文字。 </li><li data-preserve-html="true"><strong>跨屏幕的滤镜：</strong>附加了十字形星形滤镜生成器的镜头。</li><li data-preserve-html="true"><strong>跨屏幕的滤镜 - 光谱</strong>：带有带有强光谱附加的十字形星形滤波器发生器的透镜。</li><li data-preserve-html="true"><strong>跨屏幕的滤镜 - 雪花</strong> ：附加了六个方向的星形滤镜生成器的镜头。</li><li data-preserve-html="true"><strong>跨屏幕的滤镜 - 雪花光谱</strong>：带星光滤波器发生器的透镜，沿六个方向附加有强光谱。</li><li data-preserve-html="true"><strong>跨屏幕的滤镜 - 阳光</strong> ：附加了八个方向的星形滤镜生成器的镜头。</li><li data-preserve-html="true"><strong>滤光片阳光交叉光谱</strong>：带星光滤光片发生器的透镜，八个方向附加有强光谱。</li><li data-preserve-html="true"><strong>水平条纹</strong> ：此镜头眩光类型产生强烈的水平星形条纹。</li><li data-preserve-html="true"><strong>垂直条纹</strong> ：在垂直方向上具有强星形条纹的文字。 用于CCD数字相机的涂抹等。</li></ul> |

## 形状示例

![](../../assets/bloom-examples-bloom.jpg)![](../../assets/bloom-examples-standard.jpg)![](../../assets/bloom-examples-cross.jpg)![](../../assets/bloom-examples-snow.jpg)![](../../assets/bloom-examples-sunny.jpg)![](../../assets/bloom-examples-streak.jpg)
