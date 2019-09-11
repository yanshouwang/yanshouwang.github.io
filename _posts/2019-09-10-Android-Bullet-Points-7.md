---
layout: post
title: Android 开发 - 片段
date: 2019-09-10 17:11:18 +0800
categories: Android
tags: Android 开发 要点 片段
---
- `片段`用来控制屏幕的一部分。可以在多个活动中重用。

- 片段有一个与之关联的布局。

- 片段是 `android.app.Fragment` 类的一个子类。

- 每次 Android 需要一个片段的布局时，都会调用 `onCreateView()` 方法。

- 为活动的布局增加片段时，需要使用 `fragment` 元素并增加一个 `class` 属性。

- 片段生命周期方法与包含该片段的活动的状态紧密相关。

- `Fragment` 类没有扩展 `Activity` 类，也没有实现 `Context` 类。

- 片段没有 `findViewById()` 方法。实际上，要用 `getView()` 方法得到根视图的一个引用，然后调用这个视图的 `findViewById()` 方法。

- `列表片段`是提供了一个 `ListView` 的片段。可以通过派生 `ListFragment` 创建列表片段。

- 如果要让一个片段响应应用界面中的变化，可以使用 `FrameLayout` 元素。

- 使用`片段事务`对片段完成一组修改，并增加到后退堆栈。

- 可以将不同的布局放在适当的文件夹中，使应用在不同的设备上运行时有不同的外观和表现。