---
layout: post
title: Android 要点（一）
date: 2019-09-09 08:44:18 +0800
categories: Android
tags: Android 要点
---
- Android 的版本包括版本号、API 层次和代号（Android 10.0 开始取消代号）。
- `Android Studio` 是 IntelliJ IDEA 的一个特殊版本，集成了 Android 软件开发包（Android Software Developement Kit, SDK）和 `Gradle` 构建系统。
- 典型的 Android 应用由活动、布局和资源文件组成。
- 布局描述了应用是什么样，位于 app/src/main/res/layout 文件夹。
- 活动描述了应用做什么，以及如何与用户交互。你写的活动放在 app/src/main/java 文件夹中。
- `strings.xml` 包含字符串名/值对。这个文件用于将文本值与布局和活动相分离，从而支持本地化。
- `AndroidManifest.xml` 包含有关应用自身的信息。这个文件位于 app/src/main 文件夹。
- `AVD` 是一个 Android 虚拟设备。它运行在 Android 模拟器中，可以模仿真正的 Android 物理设备。
- `APK` 是一个 Android 应用包。就像是对应 Android 应用的一个 JAR 文件，包含应用的字节码、库和资源。在设备上安装应用时就是要安装 APK。
- Android 应用使用 Android 运行时环境（ART）在单独的进程中运行。
- `RelativeLayout` 用于将 GUI 组件放在布局的相对位置上。
- `TextView` 元素用于显示文本。