---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/pipeline-and-integration/configuration/command-lines.html"
breadcrumb-title: ''
description: 了解如何将命令行参数与Substance 3D Painter结合使用以实现自动化、脚本编写和管道集成。
helpx_creative_field: ""
helpx_description: Painter > Pipeline and integration > Configuration > Command lines
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 命令行
user-guide-description: ''
user-guide-title: ''
source-git-commit: 22871eab2f25d09bd82f1292d8b3e5f8c4f1c2cf
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 3%

---


# 命令行

此页面列出了一些命令行，例如，在启动应用程序创建或打开项目时可以使用这些命令行。\
这些命令行可用如下：

```
"Adobe Substance 3D Painter.exe" --command [option] 
```


## 命令列表

| 命令 | 描述 |
| --- | --- |
| **—help** **-？** **-h** | 显示有关哪些命令行可用以及如何使用这些命令行的信息。 |
| **— 版本** **— 版本** | 显示Substance 3D Painter的当前版本。 |
| **— 网格** | 在项目中加载网格。示例： `// Create a new project with a specific mesh   "Adobe Substance 3D Painter.exe" --mesh "E:/MymeshFolder/MyMesh.obj"       // Update a mesh inside an existing project   "Adobe Substance 3D Painter.exe" --mesh "E:/MymeshFolder/MyMesh.obj" "E:/MyMeshFolder/Project.spp"` |
| **—mesh-map** | 与网格相关联的已烘焙贴图（AO、法向、曲率）。 可以多次指定。 命名： TextureSetName\_AdditionalMapSlot<ul data-preserve-html="true"> <li data-preserve-html="true">环境遮蔽= <strong> <em>环境遮蔽</em> </strong></li> <li data-preserve-html="true">曲率= <strong> <em>曲率</em> </strong></li> <li data-preserve-html="true">正常= <strong> <em> normal_base </em> </strong></li> <li data-preserve-html="true">世界空间法线= <strong> <em> world_space_normals </em> </strong></li> <li data-preserve-html="true">位置= <strong> <em>位置</em> </strong></li> <li data-preserve-html="true">Thickness= <strong> <em>Thickness</em> </strong></li> <li data-preserve-html="true">ID = <em> <strong> id </strong> </em></li> </ul>示例： `"Adobe Substance 3D Painter.exe" --mesh "E:/MyMeshFolder/MyMesh.obj" --mesh-map " E:/MyMeshFolder/DefaultMaterial_ambient_occlusion.png"` |
| **—split-by-udim** | Create a texture set per UDIM tile. |
| **—export-path** | 将导出项目输出的默认导出路径。 |
| **—vram-budget** | 覆盖Substance 3D Painter引擎定义的视频内存(VRAM)预算。 “数量”以MB为单位。    示例： `// Set the VRam budget to 2GB   "Adobe Substance 3D Painter.exe" --vram-budget 2048` |
| **—disable-version-checking** | 在启动时不要检查应用程序的新版本是否可用 |
| **—enable-remote-scripting** | 允许从应用程序外部运行脚本命令。 有关详细信息，请参阅[具有脚本的远程控制](../../scripting-and-development/scripts-and-plugins/remote-control-with-scripting.md)。 |
