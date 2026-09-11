---
helpx_url: "https://helpx.adobe.com/cn/substance-3d-painter/technical-support/technical-issues/miscellaneous-issues/error-with-missing-api-ms-crt-dll.html"
breadcrumb-title: ''
description: 了解如何修复Substance 3D Painter中缺少的api-ms-crt DLL错误，以获取正确的Windows运行时库支持。
helpx_creative_field: ""
helpx_description: Painter > Technical support > Technical Issues > Miscellaneous Issues > Error with missing api-ms-crt dll
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 缺少api-ms-crt dll时出错
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# 缺少api-ms-crt dll时出错

Substance 3D Painter无法启动，因为计算机中缺少&#x200B;**api-ms-win-crt-runtime-l1-1-0.dll**。\
最有可能的原因是，作为&#x200B;**Visual C++ Redistributable** for Visual Studio 2015的一部分而提供的更新KB2999226安装失败。

## 如何修复此问题？

### 1 — 验证Windows是否为最新版本

1. 打开“开始”菜单
1. 选择“控制面板”
1. 单击&#x200B;**Windows更新**
1. 单击&#x200B;**检查更新**
1. **安装**&#x200B;所有可用更新。
1. 安装更新后，**重新启动**&#x200B;计算机。

重新启动后，再次重复上述步骤，直到没有更多更新可用。

### 2 — 安装Visual C++可再发行软件包

1. 下载Visual C++ Redistributable ：
   1. 适用于[Windows 64位](http://download.microsoft.com/download/9/3/F/93FCF1E7-E6A4-478B-96E7-D4B285925B00/vc_redist.x64.exe)
   1. 适用于[Windows 32位](http://download.microsoft.com/download/9/3/F/93FCF1E7-E6A4-478B-96E7-D4B285925B00/vc_redist.x86.exe)
1. 运行&#x200B;**vcredist\_x64.exe**（64位）或&#x200B;**vcredist\_x86.exe**（32位）
1. 选择“卸载” ，然后按照相应步骤操作
1. 再次运行可执行文件
1. 选择安装
