---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/technical-support/technical-issues/startup-issues/software-conflicts.html"
breadcrumb-title: ''
description: 了解如何解决软件冲突，从而阻止Substance 3D Painter在系统上正常启动。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > Startup Issues > Software conflicts
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 软件冲突
user-guide-description: ''
user-guide-title: ''
source-git-commit: 22871eab2f25d09bd82f1292d8b3e5f8c4f1c2cf
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---


# 软件冲突

本页列出了其他软件可能崩溃或阻止Substance 3D Painter正常运行的已知问题。

| *潜在冲突源* | *问题* |
| --- | --- |
| **防病毒/防间谍软件** | 防病毒软件或防间谍软件可能会造成以下一些问题：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>误报</b>： Painter被错误地标记为病毒或恶意软件。</li> <li data-preserve-html="true"><b>阻止的文件</b>： Painter无法读取或写入文件（导出、创建预设等）。</li> <li data-preserve-html="true"><b>文件删除</b>： Painter无法启动或正常工作，因为已删除必要的文件。</li> </ul>如果出现上述情况之一，我们建议暂时禁用防病毒软件，以查看对Painter是否有帮助或手动添加例外。 |
| **AMD CrossFire和NVIDIA SLI** | Painter不支持多个GPU配置，这会导致崩溃。 我们建议禁用此功能。 |
| <b> Autodesk助手</b> | Autodesk Assistant应用程序可能会产生冲突，并使应用程序在启动或打开项目文件时崩溃。 更新Autodesk应用程序以解决问题。 |
| <b>台Alienware/Dell计算机</b> | 请参阅此页面以了解更多信息： [打开或保存文件时崩溃](../stability-issues/crash-when-opening-or-saving-a-file.md)。 |
| **APFS by Paragon Software** | 此软件可能会在Windows路径环境变量中注册一个位置，该位置可能会在启动时使应用程序崩溃。 卸载软件可能还不够，可能需要手动删除环境变量。 有问题的位置示例： `C:Program Files (x86)Paragon SoftwareAPFS for Windowsï–›éŒ à €è¸€ì‡ì‡ç¿¹` |
| **Avecto** | 运行Avecto的早期版本可能导致速度减慢和崩溃。 确保将其更新到最新版本。 |
| **华硕GPU调整** | 该软件可能会导致Substance 3D Painter中的着色器编译期间出现问题，甚至可能会阻止着色器编译启动。 如果遇到此问题，我们建议卸载软件以查看它是否修复了问题。 |
| **华硕RAMCache** | 此软件可能会阻止Substance 3D Painter正常启动，或者使它在运行时不稳定。 如果遇到稳定性问题，我们建议您禁用或安装Asus RAMCache。 |
| **华硕Sonic套件** | 在配备ASUS主板的计算机上，默认情况下可能会安装<b>Asus Sonic Suite</b>。 卸载此软件可修复Substance 3D Painter中的一些显示/界面问题。 |
| **云备份软件** **（** OneDrive，**GDrive，** **Dropbox，** **文件流等）** | 云备份软件可能是保存项目时多次崩溃的根源。 如果发生这种情况，建议在不再进行更改时处理项目文件，并将项目文件保存到未同步的文件夹，改为将项目文件复制回云驱动器。 |
| **复选框** | 该软件会在打开文件对话框（如打开或保存项目）时制造冲突并导致应用程序崩溃。 您可以在复选框首选项中禁用设置<b>启用桌面模型的缩览图预览</b>以避免此问题。 |
| **Duet显示** | <b>Duet Display</b>已知会产生GPU驱动程序问题，可能会影响Substance 3D Painter的行为。 建议卸载它。 |
| **Google Chrome** | Google Chrome在与Substance 3D Painter一起运行时，可能会导致一些崩溃。 要提高Substance 3D Painter的稳定性，建议您更新Google Chrome和GPU驱动程序。 如果仍然发生崩溃，请在Google Chrome中禁用硬件加速（这将阻止Chrome使用GPU）。 |
| **Nahimic音频软件** | <b>Nahimic</b>可能会冻结或崩溃Painter。 停止它会有帮助，更新它也会避免问题。 Nahimic还会运行后台服务，这些服务可能会干扰应用程序，可能需要停止或禁用。 |
| **Openshot视频软件** | <b>Openshot视频软件</b>可能会使用书架预览与Substance 3D Painter发生冲突。 更新Openshot应该可以修复此问题。 |
| **Pyinstaller** | 此应用程序会产生不正确的环境设置，导致启动时出错。 有关详细信息，请参阅[应用程序因Qt](application-failed-to-start-because-of-qt.md)而无法启动。 |
| **Rptr / Plays.tv** | 默认情况下，<b>Rptr</b>(或<b>[Plays.tv](http://plays.tv/) </b>)与某些GPU驱动程序一起安装。 此软件可能会造成应用程序不稳定和崩溃。 建议卸载该应用程序。 |
| **RGBFusion** | 此软件可能会与图形输入板驱动程序发生冲突，停止该过程可能会暂时修复该问题，或者卸载RGBFusion以进行永久修复。 |
