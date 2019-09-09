---
layout: post
title: Android 开发 - 活动生命周期
date: 2019-09-09 14:22:18 +0800
categories: Android
tags: Android 开发 要点 活动 生命周期
---
- 默认地，每个应用都在自己的进程中运行。

- 只有主线程可以更新用户界面。

- 可以使用 `Handler` 调度代码，或者将代码提交到一个不同的线程。

- 设备配置的变化会导致活动撤销然后重新创建。

- 活动从 `Activity` 类继承了活动生命周期方法。如果要覆盖其中某个方法，首先需要调用超类中的相应方法。

-  `onSaveInstanceState(bundle)` 允许在活动撤销之前先保存它的状态。可以使用 `bundle` 在 `onCreate()` 中恢复这个状态。

- 可以使用 `bundle.put*("name", value)` 将值增加到一个 `bundle`。

- 可以使用 `bundle.get*("name")` 从 `bundle` 获取值。

- `onCreate()` 和 `onDestroy()` 分别处理活动的生与死。

- `onRestart()`、`onStart()` 和 `onStop()` 处理活动的可见性。

- `onResume()` 和 `onPause()` 处理活动得到和失去焦点时的状态。