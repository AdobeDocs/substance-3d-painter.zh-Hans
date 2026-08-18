---
helpx_url: "https://helpx.adobe.com/substance-3d-painter/technical-support/technical-issues/miscellaneous-issues/impossible-to-use-the-alt-keyboard-shortcut-on-linux.html"
breadcrumb-title: ''
description: 了解如何在Substance 3D Painter中修复Linux上的ALT键盘快捷键问题，以便正确进行键盘导航。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > Miscellaneous Issues > Impossible to use the ALT keyboard shortcut on Linux
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 无法在Linux上使用ALT键盘快捷键
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---


# 无法在Linux上使用ALT键盘快捷键

如果您正在运行使用&#x200B;**Gnome**&#x200B;作为用户界面的Linux分发（**Ubuntu**&#x200B;或&#x200B;**CentOS**），则可能需要禁用&#x200B;**ALT**&#x200B;键的默认行为以便能够在视口中导航。

## CentOS

1 — 转到&#x200B;**系统> Windows**

![](../../../assets/centos-window.png){width="250px"}

2 — 将“移动键”设置更改为“**Alt**”以外的其他设置。 例如，使用“ **超级**”（选择键盘的“Windows”键）。

![](../../../assets/centos-setting.png){width="350px"}

## 乌班图

1 — 打开终端并运行以下命令：

```
sudo apt-get install dconf-tools
```


这将安装高级配置工具，您可能必须允许安装其他依赖项才能运行它。

2 — 打开“开始”菜单并查找“ **Dconf-tools**”。 启动。

3 — 通过转到以下路径来展开左侧的树菜单： **组织> gnome >桌面> wm >首选项**

4 — 编辑“mouse-button-modifier”并更改其值。 请设置或改为设置，但&#x200B;*不要将其留空* 。 Super等同于“Windows”键。

![](../../../assets/ubuntu-setting.png){width="500px"}
