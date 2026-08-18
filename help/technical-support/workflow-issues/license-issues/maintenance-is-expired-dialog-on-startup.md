---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/workflow-issues/license-issues/maintenance-is-expired-dialog-on-startup.html"
breadcrumb-title: ''
description: 了解如何解决Substance 3D Painter启动时显示的“维护已过期”对话框，以便进行许可证管理。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Workflow Issues > License Issues > Maintenance is expired dialog on startup
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 启动时显示“维护已过期”对话框
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 1%

---


# 启动时显示“维护已过期”对话框

![](../../../assets/expired-mainteance-message.png)

启动应用程序时，可能会显示一个对话框，其中显示“您的当前维护已过期”消息。 本页列出了有关如何避免此对话框的解决方案。

## 解决方案1：更新许可证文件

出现警告消息是因为许可证文件太旧，需要更新。 为此，只需通过应用程序向导&#x200B;**重新激活产品**&#x200B;即可。 也可以通过Substance 3D网站<https://www.substance3d.com/>手动下载许可证文件。

## 解决方案2：编辑首选项设置以隐藏对话框

>[!NOTE]
>
> 我们建议先尝试更新许可证文件，然后再使用此替代解决方案。

另一种解决方法是通过设置特定设置来隐藏警告消息。

导航到应用程序首选项位置：

<table data-preserve-html="true"><colgroup> <col/> <col/> <col/> </colgroup><tbody><tr><th>系统</th><th>Version</th><th>路径</th></tr><tr><td rowspan="2"><p><strong>Windows</strong></p><p>（注册表）</p></td><td><strong>7.2</strong>或更高版本</td><td>HKEY_CURRENT_USER\Software\Adobe\Adobe Substance 3D Painter</td></tr><tr><td>旧版</td><td>HKEY_CURRENT_USER\Software\Allegorithmic\Substance Painter</td></tr><tr><td rowspan="2"><p><strong>Mac</strong></p><p>（库）</p></td><td><strong>7.2</strong>或更高版本</td><td>/用户/[用户名]/Library/Preferences/com.adobe.Adobe Substance 3D Painter.plist</td></tr><tr><td>旧版</td><td>/用户/[用户名]/资源库/Library/Preferences/com.substance3d.Substance Painter.plist</td></tr><tr><td rowspan="2"><strong>Linux</strong></td><td><strong>7.2</strong>或更高版本</td><td>/home/[用户名]/.config/Adobe/Adobe Substance 3D Painter.conf</td></tr><tr><td>旧版</td><td>/home/[用户名]/.config/Allegorithmic/Substance Painter.conf</td></tr></tbody></table>

### Windows

要在Windows上设置变量，请执行以下步骤：

1. 打开开始菜单。
1. 搜索&#x200B;**Regedit**&#x200B;以打开注册表编辑器。
1. 导航到上表中列出的注册表项。
1. 单击左侧树形视图中名为software的注册表项。
1. 右键单击右侧面板中的空白区域，然后选择&#x200B;**新建>字符串值**。
1. 将新值命名为&#x200B;**DisableLicenseWarningPopup**，然后按Enter进行验证。
1. 双击刚刚创建的值。
1. 将值数据字段设置为： **true**
1. 保存更改。
1. 启动应用程序。

### macOS

1. 打开新的&#x200B;**查找器**&#x200B;窗口
1. 导航到上表中列出的路径。
1. 右键单击&#x200B;**plist**&#x200B;文件，然后选择&#x200B;**打开方式> Xcode**。
1. 在列表顶部，添加名为&#x200B;**DisableLicenseWarningPopup**&#x200B;的新密钥
1. 将密钥类型设置为&#x200B;**字符串**
1. 将键值设置为&#x200B;**true**
1. 保存并关闭文件。
1. 启动应用程序。

### Linux

要在Linux上设置变量，请执行以下步骤：

1. 导航到上表中的路径列表。
1. 打开文件夹中的&#x200B;**.conf**&#x200B;文件。
1. 在第&#x200B;**[常规]**&#x200B;行下添加新行
1. 在新行上粘贴以下文本： **DisableLicenseWarningPopup=true**
1. 保存文件。
1. 启动应用程序。
