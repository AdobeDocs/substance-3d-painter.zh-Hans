---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/pipeline-and-integration/configuration/environment-variables.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中使用环境变量来配置应用程序行为和管道集成。
helpx_creative_field: ""
helpx_description: Painter > Pipeline and integration > Configuration > Environment variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 环境变量
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 3%

---


# 环境变量

此页列出可用于覆盖应用程序的默认行为的环境变量。

| 变量 | 描述 | Version |
| --- | --- | --- |
| **SUBSTANCE\_PAINTER\_LICENSE** | 值：到许可证文件本身的直接路径。允许覆盖许可证文件的默认位置。 示例：如果许可证文件位于&#x200B;**H：/allegorithmic/licenses/substance\_painter.key**&#x200B;上，则变量数据应为&#x200B;**&quot;H：/allegorithmic/licenses/substance\_painter.key&quot;**。  **注意：**&#x200B;请改用SUBSTANCE\_PAINTER\_2\_LICENSE作为3.x (2017.x)之前的版本。 | <ol data-preserve-html="true"><li data-preserve-html="true">1</li></ol> |
| **ALLEGO\_LICENSE\_IDLE\_DELAY** | 值： 7200指定在多用户配置的情况下，在释放许可证席位之前的秒数。 默认值为2小时（7200秒）。 | <ol data-preserve-html="true"><li data-preserve-html="true">1</li></ol> |
| **ALG\_PAINTER\_SKIP\_CHECK\_FOR\_UPDATES** | 值： 0或1 （1 =禁用更新检查）允许在应用程序启动时跳过更新检查。 禁用新增功能面板。 | <ol data-preserve-html="true"><li data-preserve-html="true">2.2</li></ol> |
| **SUBSTANCE\_PAINTER\_SVT\_HARDWARE\_ACCELERATION** | 值： 0或1 （1 =启用）使用GPU上的稀疏功能。 如果GPU或操作系统不支持此设置，则会将其忽略。 有关兼容的硬件配置，请参阅文档： [稀疏虚拟纹理](../../features/sparse-virtual-textures.md)此变量将覆盖[设置](../../interface/settings/settings.md)窗口中可用的参数。 | <ol data-preserve-html="true"><li data-preserve-html="true">3</li></ol> |
| **SUBSTANCE\_PAINTER\_TEMP\_LOCATION** | 值：文件夹的直接路径定义Substance Painter应将其临时文件（包括SVT缓存）写入的位置。此变量将覆盖[设置](../../interface/settings/settings.md)窗口中可用的参数。 | <ol data-preserve-html="true"><li data-preserve-html="true">3</li></ol> |
| **SUBSTANCE\_PAINTER\_PREVIEWS\_MEMORY\_BUDGET** | 值： 500定义应用程序可用于从“资源”窗口加载和临时存储预览的内存(Ram)量。 达到预算限制时，旧预览会被卸载。 此值仅控制“资源”窗口中的预览显示。该值以MB为单位定义。 默认值为500MB。 | <ol data-preserve-html="true"><li data-preserve-html="true">2</li></ol> |
| **SUBSTANCE\_PAINTER\_PLUGINS\_PATH** | 其他Python插件的位置。 | 6.1 |
| **PYTHONPATH** | 其他Python模块，通过Python集成应用程序加载。 有关详细信息，请参阅[加载外部Python模块](https://helpx.adobe.com/cn/substance-3d/unlisted/documentation/spdoc/loading-external-python-modules-205363420.html)。 | <ol data-preserve-html="true"><li data-preserve-html="true">1</li></ol> |
| **OCIO** | **config.ocio**&#x200B;文件的路径，该文件将用于使用OpenColorIO驱动[色彩管理](../../features/color-management/color-management.md)设置。  **注意：**&#x200B;此环境变量的优先级高于&#x200B;**PAINTER\_ACE\_CONFIG**&#x200B;变量。 | <ol data-preserve-html="true"><li data-preserve-html="true">4</li></ol> |
| **PAINTER\_ACE\_CONFIG** | 用于通过AdobeACE驱动[色彩管理](../../features/color-management/color-management.md)设置的json文件的路径。 | <ol data-preserve-html="true"><li data-preserve-html="true">1</li></ol> |
| **SUBSTANCE\_DISABLE\_SPECIFIC\_FEATURES** | 禁用应用程序中的多项功能：<ul data-preserve-html="true"><li data-preserve-html="true">外部资源（帮助、网页、示例等）链接</li><li data-preserve-html="true">禁用更新检查</li><li data-preserve-html="true">禁用使用情况统计信息的发送</li><li data-preserve-html="true">禁用导出到Substance share</li><li data-preserve-html="true">禁用“欢迎”和“新增功能”面板</li></ul> | <ol data-preserve-html="true"><li data-preserve-html="true">1</li></ol> |
| **ALG\_PAINTER\_DEBUG\_FPS** | 在视区内部显示一个计数器，指示视区每秒渲染多少帧。 | <ol data-preserve-html="true"><li data-preserve-html="true">1</li></ol> |
| **SUBSTANCE\_PAINTER\_VRAM\_BUDGET** | 指定Painter可以使用的GPU内存量。 这将定义全球预算（以MB为单位）。 例如，要定义4GB的限制，请使用值4000。命令行参数也可用于执行相同的操作。 请参阅[命令行](command-lines.md)。 | <ol data-preserve-html="true"><li data-preserve-html="true">2.1</li></ol> |
