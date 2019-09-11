---
layout: post
title: Android 开发 - 嵌套片段
date: 2019-09-11 14:13:18 +0800
categories: Android
tags: Android 开发 要点 片段 嵌套
---
- 片段可以包含其他片段。

- 如果在一个片段中嵌套另一个片段，需要通过编程在 Java 代码中增加这个嵌套片段。

- 在一个嵌套片段上执行事务时，要使用 `getChildFragmentManager()` 创建事务。

- 如果在片段中使用 `android:onClick` 属性，Android 会在这个片段的父活动中查找同名的方法。

- 不要在片段中使用 `android:onClick` 属性，而应当让片段实现 `View.OnClickListener` 接口，并实现它的 `onClick()` 方法。

- 设备配置改变时，活动和它的片段会被撤销。活动重新创建时，它会在 `onCreate()` 方法的 `setContentView()` 调用中重放它的片段事务。

- 活动重放片段事务之后会运行片段的 `onCreateView()` 方法。