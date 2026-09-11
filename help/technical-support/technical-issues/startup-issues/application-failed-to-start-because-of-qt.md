---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/technical-issues/startup-issues/application-failed-to-start-because-of-qt.html"
breadcrumb-title: ''
description: 了解如何修复由Qt框架问题导致的Substance 3D Painter启动失败以正确启动应用程序。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > Startup Issues > Application failed to start because of Qt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 由于Qt，应用程序无法启动
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---


# 由于Qt，应用程序无法启动

启动应用程序时可能会出现以下错误消息：

>> 

此应用程序无法启动，因为无法初始化Qt平台插件。 重新安装应用程序可以修复此问题。

可用的平台增效工具包括：最小、屏幕外、webgl、windows。

此错误可能是因为另一个软件定义的环境变量与应用程序冲突。

在启动应用程序之前，请确保从当前环境中删除以下变量：

```
QT_PLUGIN_PATH 

QML2_IMPORT_PATH
```


>[!NOTE]
>
> 这些变量也可以从Python上下文中继承，例如&#x200B;**pyinstaller**。 确保从启动应用程序的上下文中删除它们。
