---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/interface/assets/advanced-search-queries.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中创建高级搜索查询，以使用复杂的搜索条件查找特定资源。
helpx_creative_field: ""
helpx_description: Painter > Interface > Assets > Advanced search queries
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 高级搜索查询
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---


# 高级搜索查询

高级搜索查询允许您构建复杂的搜索，并将它们作为[保存的搜索](saved-searches.md)重复使用。

高级查询可以在搜索栏中使用，并且可以包含 — 

1. **路径** ：允许按文件夹/文件夹结构优化搜索结果。
1. **用法** ：列出应用程序中可用的所有可能用法
1. **文本查询** ：允许自由添加任何其他类型的查询（如自定义关键字）

定义新的搜索查询时允许进行多项选择。

## 路径

路径查询允许基于路径优化查询。 **按路径筛选**&#x200B;面板列出了所有可用的库（可通过“编辑”>“设置”>“库”自行添加）。\
可以使用路径定义按自定义库路径或层次结构中的特定子文件夹进行筛选。

## 使用情况

使用情况定义什么是资源以及如何在Substance 3D Painter中使用资源。 有些可由资源的文件类型定义。\
例如：

* **pbr.glsl**：着色器文件 — 它只能用作着色器，不能用作其他内容。
* **effect.sbsar**： Substance文件 — 可以是生成器、滤镜甚至素材，因此如果原始图形（在Designer中）中未设置其用法，则导入时用户必须在Painter中指示它。

## 文本

文本查询支持多种过滤类型，其中一些过滤类型比常规界面更高级。\
键入正确的关键字即可启用这些功能。

* **可用的搜索类型** ：
  * “ **n：** ”：名称
  * “ **：**”：托架/库（包括“会话”和“项目”）
  * “ **p：** ”：路径
  * “ **u：** ”：用法
* **转义** ：可以在需要转义的字符前使用“ **\**”或改用引号，例如：
  * **a\ name\ with\ spaces**
  * **“具有空格的名称”**
* **特定属性（或组）** ：要在特定属性中进行搜索，请在类型说明符前加上“或组”。 示例：
  * **n:a，b，c，d** ： name是a、b、c或d
* **搜索行为** ：
  * 要筛选特定用法，请将特定的&#x200B;**关键字**&#x200B;添加到您的搜索中，例如：“**图像**&#x200B;周围环境”
  * 要添加多个请求，请使用逗号“ **，**”，例如： “cobalt **，** gold”（如果使用逗号，则搜索将仅显示同时匹配两个关键字的资源）
  * 要搜索确切的名称，请使用感叹号“！” 在结尾处，示例： **di！**  （将返回&#x200B;**Dirt**，但不返回&#x200B;**滴**，此关键字将禁用模糊匹配）
  * 要从搜索中排除图案，请使用连字符“ **-**”，例如： **u:image n：-normal**（将返回不包含“normal”的图像）
* **匹配函数（模式后缀） ：**
  * **默认** ：近似匹配（模糊）
  * **包含** ： ！
  * **正则表达式** ： #
  * **等于** ： =
  * **以**&#x200B;开头： ^
  * **以**&#x200B;结尾： &amp;
