---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/painting/text-resource.html"
breadcrumb-title: ''
description: 了解如何使用Substance 3D Painter中的文本资源向纹理绘画工作流程添加文本和排版规则。
helpx_creative_field: ""
helpx_description: Substance 3D Painter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 文本资源
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%

---


# 文本资源

![](../assets/v10_text_resource_banner-1.jpg)

中的<b>文本资源</b>可用于使用特定的<b>字体文件</b>将文本写入纹理。 有多个参数可用于调整最终文本绘制的外观。

## 浏览字体

要浏览可用的字体文件，只需单击[资源窗口](../interface/assets/assets.md)中的字体过滤器（<b>T</b>按钮）即可：

![](../assets/v10_text_assets.png)

字体还可以根据其在系统中的位置按路径过滤：

![](../assets/v10_font_path.png)

可用的字体位置取决于当前操作系统：

|  |  |
| --- | --- |
| Windows | <ul data-preserve-html="true"> <li data-preserve-html="true"><b>系统</b>： C：/Windows/Fonts</li> <li data-preserve-html="true"><b>用户</b>：C：/Users/username/Appdata/Local/Microsoft/Windows/Fonts</li> </ul> |
| macOS | <ul data-preserve-html="true"> <li data-preserve-html="true"><b>系统</b>： /系统/资源库/Fonts</li> <li data-preserve-html="true"><b>本地</b>： /Library/Fonts</li> <li data-preserve-html="true"><b>用户</b>： /用户/用户名/资源库/Fonts</li> </ul> |
| Linux | <ul data-preserve-html="true"> <li data-preserve-html="true"><b>系统</b>： /usr/share/fonts/</li> <li data-preserve-html="true"><b>本地</b>： /usr/local/share/fonts/</li> <li data-preserve-html="true"><b>用户</b>： /home/username/.local/share/fonts/</li> </ul> |

### 导入字体

与任何常规资源一样，字体可以手动导入或放入现有的Painter库中。 为此，请参阅[导入文档](../content/importing-assets/import-drag-and-drop.md)。

Painter同时支持<b>.ttf</b>和<b>.otf</b>两种字体格式。

>[!NOTE]
>
> 如果资源无法加载/导入，并显示“由于字体的许可限制而无法导入”错误消息，则表明Painter无法使用该资源。 只能使用其元数据中标记为<b>可嵌入</b>的字体。

### 将字体用作文本资源

纹理资源的工作方式与其他资源（例如图像或Substance素材）类似，并且可用于画笔参数、填充投影或Substance图像输入。

要创建文本资源，只需将字体添加到资源插槽中即可。 还可以在视区中拖放字体。

![](../assets/v10_text_drag_drop.gif)

### 文本资源参数

文本资源具有以下基本参数：

![](../assets/v10_text_params_base.png)

| <b>参数</b> | <b>描述</b> |
| --- | --- |
| <b>文本</b> | 要渲染的文本。  **注意：**&#x200B;界面中的文本字段使用带有多种字符的通用字体，这可能会导致在字段中键入的内容与所选字体能够在纹理中呈现的内容不一致。 |
| <b>字体大小</b> | 指定用于计算字体大小的模式。 可用模式包括：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>自动</b>：根据文本内容自动计算大小并适合纹理。</li> <li data-preserve-html="true"><b>自定义</b>：可以通过专用设置手动控制大小。</li> </ul> |
| <b>对齐</b> | 控制垂直和水平对齐方式。 使用按钮选择要使用的模式。 |
| <b>颜色</b> | 渲染文本的颜色。 如果在蒙版或灰度通道中使用文本资源，则此设置可能是灰度设置。 |

还提供更高级的参数：

![](../assets/v10_text_params_advanced.png)

| <b>参数</b> | <b>描述</b> |
| --- | --- |
| <b>行距</b> | 文本行之间的距离（“行距”）相对于字体大小。 |
| <b>字符间距</b> | 相邻字符之间相对于字体大小的间距大小。 可以为负值以减去间距。 |
| <b>偏移</b> | 文本的水平和垂直偏移。 规范化为字体大小。 |
| <b>背景填充</b> | 文本后面的背景颜色。 |
| <b>背景不透明度</b> | 背景颜色的可见程度。 |
| <b>分辨率</b> | 指定用于计算渲染文本所用纹理大小的模式。 可用模式包括：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>自动</b>：分辨率是自动计算的。</li> <li data-preserve-html="true"><b>自定义</b>：可通过专用设置手动定义分辨率。</li> </ul> |
