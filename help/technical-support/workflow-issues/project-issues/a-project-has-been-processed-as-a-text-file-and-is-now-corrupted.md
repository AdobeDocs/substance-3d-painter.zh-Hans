---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/workflow-issues/project-issues/a-project-has-been-processed-as-a-text-file-and-is-now-corrupted.html"
breadcrumb-title: ''
description: 了解如何恢复已损坏的、作为文本文件处理的Substance 3D Painter项目文件。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Workflow Issues > Project Issues > Corrupted project file
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 损坏的项目文件
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---


# 项目已作为文本文件处理，现在已损坏

有时，加载项目时可能会出现以下错误：

```
[Hdf5Archive] Archive 'project.spp' appears to have been processed as a text file and is irremediably corrupted. 

[Project management] The selected project 'project.spp' isn't valid!
```


此错误表示已在Substance 3D Painter之外修改了项目，因此&#x200B;**无法正确读回** 。\
当版本控制软件（如&#x200B;**Perforce** ）将Substance 3D Painter项目&#x200B;**处理为文本文件而不是二进制文件**&#x200B;时，通常会发生这种情况。 唯一的解决方案是向版本控制软件添加新的规则/例外，以强制将&#x200B;**spp文件作为二进制文件**&#x200B;进行处理。 有关&#x200B;**性能**&#x200B;的详细信息，请参阅专用文档： <https://www.perforce.com/perforce/r16.1/manuals/cmdref/p4_typemap.html>
