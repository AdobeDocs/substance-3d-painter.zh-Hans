---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/pipeline-and-integration/resource-management/adding-resource-paths-by-editing-preferences-manually/editing-resource-paths-manually.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter首选项中手动编辑资源路径以自定义托架资源位置。
helpx_creative_field: ""
helpx_description: Painter > Pipeline and integration > Resource management > Adding resource paths by editing preferences manually > Editing resource paths manually
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 手动编辑资源路径
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 1%

---


# 手动编辑资源路径

本页提供了如何编辑首选项以在不启动应用程序的情况下添加或删除资源路径的指南。

## 首选项位置

使用应用程序首选项管理资源位置，这些首选项可根据平台而更改：

<table data-preserve-html="true"> <colgroup> <col/> <col/> <col/> </colgroup> <tbody> <tr> <th>系统</th> <th>Version</th> <th>路径</th> </tr> <tr> <td rowspan="2"><p><strong>Windows</strong></p><p>（注册表）</p></td> <td><strong>7.2</strong>或更高版本</td> <td>HKEY_CURRENT_USER\Software\Adobe\Adobe Substance 3D Painter</td> </tr> <tr> <td>旧版</td> <td>HKEY_CURRENT_USER\Software\Allegorithmic\Substance Painter</td> </tr> <tr> <td rowspan="2"><p><strong>Mac</strong></p><p>（库）</p></td> <td><strong>7.2</strong>或更高版本</td> <td>/用户/[用户名]/Library/Preferences/com.adobe.Adobe Substance 3D Painter.plist</td> </tr> <tr> <td>旧版</td> <td>/用户/[用户名]/资源库/Library/Preferences/com.substance3d.Substance Painter.plist</td> </tr> <tr> <td rowspan="2"><strong>Linux</strong></td> <td><strong>7.2</strong>或更高版本</td> <td>/home/[用户名]/.config/Adobe/Adobe Substance 3D Painter.conf</td> </tr> <tr> <td>旧版</td> <td>/home/[用户名]/.config/Allegorithmic/Substance Painter.conf</td> </tr> </tbody> </table>

## 在Windows上添加路径

在Windows上，可以通过Windows注册表管理路径：

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../assets/reg-shelf-pathinfos.png)

</td>
<td style="border: 0;" valign="top">

![](../../../assets/reg-content.png)

</td>
</tr>
</table>

1. 单击&#x200B;**开始>运行**&#x200B;或按&#x200B;**Windows + R** 。
1. 在对话框中键入“**regedit**”（不带引号），然后按&#x200B;**确定**。
1. 在&#x200B;**注册表编辑器**&#x200B;窗口左侧的树形视图中导航，然后转到上述注册表项。
1. **在** pathInfos **下面添加一个密钥**，并以&#x200B;**数字**&#x200B;作为名称。 根据现有键递增编号（从1开始）。
1. 在窗口右侧执行&#x200B;**右键单击** > **新建** > **字符串值**。 将其命名为&#x200B;**已禁用**&#x200B;并将值设置为&#x200B;**false**。
1. 在窗口右侧执行&#x200B;**右键单击** > **新建** > **字符串值**。 将其命名为&#x200B;**name**&#x200B;并输入自定义托架的名称。
1. 在窗口右侧执行&#x200B;**右键单击** > **新建** > **字符串值**。 将其命名为&#x200B;**path**，并将值设置为盘架所在的path。
1. 不要忘记在“**pathInfos**”内按1递增键“**size**”。
1. 关闭窗口。
1. 启动应用程序。

通过将条目&#x200B;**writableShelf**&#x200B;的值更改为新位置的名称，可以将新路径定义为默认路径（像创建预设一样创建新资源时）。

![](../../../assets/default-shelf.png)

## 在Linux上添加路径

在&#x200B;**Linux**&#x200B;上，可以通过用户应用程序首选项配置文件创建其他路径，该文件存储在主目录中(请参阅。

1. 导航到上述路径。
1. 打开文件&#x200B;**Substance 3D Painter.config**
1. 向下滚动到&#x200B;**[托架]**&#x200B;部分

通过递增最后一个可见编号来添加新托架路径，例如：

```
pathInfos2disabled=false  

pathInfos2name=custom_resources 

pathInfos2path=/home/Username/Documents/custom_path 

writableShelf=custom_resources
```


使用&#x200B;**writableShelf**&#x200B;变量指定哪个路径将是默认路径（如果创建了新资源，例如预设）。

保存更改并重新启动应用程序。
