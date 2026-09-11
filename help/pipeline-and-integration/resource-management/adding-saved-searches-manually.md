---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/pipeline-and-integration/resource-management/adding-saved-searches-manually.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中手动添加保存的搜索以快速访问常用资源筛选器。
helpx_creative_field: ""
helpx_description: Painter > Pipeline and integration > Resource management > Adding saved searches manually
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 手动添加保存的搜索
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 2%

---


# 手动添加保存的搜索

可通过编辑配置文件来定义资源搜索查询（或保存的搜索）。 本页介绍操作方法。

## 配置文件的位置

要添加自定义保存的查询，请导航到用户的“文档”文件夹并打开&#x200B;**Shelf.ini**&#x200B;文件。

<table data-preserve-html="true" style="width: 100.0%;"> <colgroup> <col style="width: 15.0%;"/> <col style="width: 15.0%;"/> <col style="width: 70.0%;"/> </colgroup> <tbody> <tr> <th>Platform</th> <th>Version</th> <th>路径</th> </tr> <tr> <td rowspan="2"><strong>Windows</strong></td> <td><strong>7.2</strong>或更高版本</td> <td colspan="1">C:\Users\username\Documents\Adobe\Adobe Substance 3D Painter</td> </tr> <tr> <td colspan="1">旧版</td> <td colspan="1">C:\Users\username\Documents\Allegorithmic\Substance Painter</td> </tr> <tr> <td rowspan="2"><strong>Mac</strong></td> <td colspan="1"><strong>7.2</strong>或更高版本</td> <td colspan="1">/用户/用户名/文稿/Adobe/Adobe Substance 3D Painter</td> </tr> <tr> <td colspan="1">旧版</td> <td colspan="1">/Users/用户名/Documents/Allegorithmic/Substance Painter</td> </tr> <tr> <td rowspan="2"><strong>Linux</strong></td> <td colspan="1"><strong>7.2</strong>或更高版本</td> <td colspan="1">/home/username/Documents/Adobe/Adobe Substance 3D Painter</td> </tr> <tr> <td>旧版</td> <td colspan="1">/home/username/Documents/Allegorithmic/Substance Painter</td> </tr> </tbody> </table>

## 示例

以下是可以放入配置文件中的内容示例：

```
[filters] 

size=4 

1name=Grunge 

1query="u:basematerial=,smartmaterial=,smartmask=,texture=,procedural=,brush=,alpha= grunge" 

2name=Procedural 

2query="u:procedural=" 

3name=Environment 

3query="u:environment=" 

4name=Default Filters 

4query="p:/allegorithmic/^ u:filters="
```


语法如下所示：

* **大小**：确定应用程序需要读取和加载的自定义预设的数量。
* **数字**：在行的开始处定义它指向的当前预设（例如： **1/**）。
* **查询**： （在数字之后）定义实际使用的搜索词。 在示例中，它使用&#x200B;**u：**&#x200B;作为用法，**p：**&#x200B;作为路径，或字符串作为搜索词。 查询内容必须用引号括起来。 若要了解可以使用的术语，[请参阅此页面](../../interface/assets/advanced-search-queries.md)。
* **名称**：预设的名称。
