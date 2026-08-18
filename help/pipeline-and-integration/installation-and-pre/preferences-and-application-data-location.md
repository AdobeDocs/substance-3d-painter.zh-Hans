---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/pipeline-and-integration/installation-and-preferences/preferences-and-application-data-location.html"
breadcrumb-title: ''
description: 了解Substance 3D Painter的首选项和应用程序数据位置，以管理设置和用户数据。
helpx_creative_field: ""
helpx_description: Painter > Pipeline and integration > Installation and preferences > Preferences and application data location
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 首选项和应用程序数据位置
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 4%

---


# 首选项和应用程序数据位置

此页将有关每个版本和平台存储应用程序首选项的位置的信息重新分组。\
了解首选项的存储位置可能会很有用，以防您要添加&#x200B;**自定义搁板**（对于Studio安装）或删除这些首选项以执行应用程序的&#x200B;**全新安装**。

## 首选项

此路径是应用程序首选项（已保存的快捷键、托架/资源路径、界面布局等）的位置。

<table data-preserve-html="true"><colgroup> <col/> <col/> <col/> </colgroup><tbody><tr><th>系统</th><th>Version</th><th>路径</th></tr><tr><td rowspan="2"><p><strong>Windows</strong></p><p>（注册表）</p></td><td><strong>7.2</strong>或更高版本</td><td>HKEY_CURRENT_USER\Software\Adobe\Adobe Substance 3D Painter</td></tr><tr><td>旧版</td><td>HKEY_CURRENT_USER\Software\Allegorithmic\Substance Painter</td></tr><tr><td rowspan="2"><p><strong>Mac</strong></p><p>（库）</p></td><td><strong>7.2</strong>或更高版本</td><td>/用户/[用户名]/Library/Preferences/com.adobe.Adobe Substance 3D Painter.plist</td></tr><tr><td>旧版</td><td>/用户/[用户名]/资源库/Library/Preferences/com.substance3d.Substance Painter.plist</td></tr><tr><td rowspan="2"><strong>Linux</strong></td><td><strong>7.2</strong>或更高版本</td><td>/home/[用户名]/.config/Adobe/Adobe Substance 3D Painter.conf</td></tr><tr><td>旧版</td><td>/home/[用户名]/.config/Allegorithmic/Substance Painter.conf</td></tr></tbody></table>

## 应用程序数据

此路径是其他应用程序数据（资源缩略图、日志文件等）的位置。

<table data-preserve-html="true"><colgroup> <col/> <col/> <col/> <col/> </colgroup><tbody><tr><th>Platform</th><th>Version</th><th colspan="2">路径</th></tr><tr><td rowspan="4"><strong>Windows</strong></td><td rowspan="2"><strong>7.2</strong>或更高版本</td><td colspan="1">应用程序数据（本地）</td><td colspan="1">C:\Users\用户\[用户名]\AppData\Local\Adobe\Adobe Substance 3D Painter</td></tr><tr><td colspan="1">应用程序数据（漫游）</td><td colspan="1">C:\Users\用户\[用户名]\AppData\Roaming\Adobe\Adobe Substance 3D Painter</td></tr><tr><td rowspan="2">旧版</td><td colspan="1">应用程序数据（本地）</td><td colspan="1">C:\Users\用户\[用户名]\AppData\Local\Allegorithmic\Substance Painter</td></tr><tr><td colspan="1">应用程序数据（漫游）</td><td colspan="1">C:\Users\用户\[用户名]\AppData\Roaming\Allegorithmic\Substance Painter</td></tr><tr><td rowspan="2"><strong>Mac</strong></td><td colspan="1"><strong>7.2</strong>或更高版本</td><td colspan="2">/用户/[用户名]/资源库/Application Support/Adobe/Adobe Substance 3D Painter</td></tr><tr><td colspan="1">旧版</td><td colspan="2">/用户/[用户名]/资源库/Application Support/Allegorithmic/Substance Painter</td></tr><tr><td rowspan="2"><strong>Linux</strong></td><td colspan="1"><strong>7.2</strong>或更高版本</td><td colspan="2">/home/[用户名]/.local/share/Adobe/Adobe Substance 3D Painter</td></tr><tr><td>旧版</td><td colspan="2">/home/[用户名]/.local/share/Allegorithmic/Substance Painter</td></tr></tbody></table>

>[!NOTE]
>
> 上述路径中的某些目录可能默认处于隐藏状态。 在文件资源管理器中手动键入路径，或者显示隐藏的文件以查看它们。
