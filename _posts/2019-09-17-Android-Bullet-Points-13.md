---
layout: post
title: Android 开发 - 服务
date: 2019-09-17 13:06:18 +0800
categories: Android
tags: Android 开发 要点 服务
---
- `服务`是可以在后台完成任务的组件。服务没有用户界面。

- `启动服务`可以在后台无限期的运行，甚至启动这个服务的活动已经撤销也不会有影响。一旦操作完成，它会自行停止。

- 要使用 `service` 元素在 `AndroidManifest.xml` 中声明服务。

- 可以扩展 `IntentService` 类并覆盖它的 `onHandleIntent()` 方法创建一个简单的启动服务。 `IntentService` 类设计用来处理意图。

- 可以使用 `startService()` 方法启动一个启动服务。

- 如果覆盖 `IntentService` 的 `onStartCommand` 方法，必须调用它的超类实现。

- 可以使用`通知生成器`创建一个通知。使用挂起意图让通知启动一个活动。然后使用 Android 的通知服务来显示通知。

- `绑定服务`绑定到另一个组件（如一个活动）。活动可以与它交互，并得到结果。

- 通常通过扩展 `Service` 类来创建绑定服务。必须定义你自己的 `Binder` 对象，并覆盖 `onBind()` 方法。组件希望绑定到服务时会调用这个方法。

- 创建服务时会调用 `Service` 的 `onCreate()` 方法。使用这个方法来完成实例化。

- 服务将要撤销时会调用 `Service` 的 `onDestroy()` 方法。

- 可以使用 `Android 位置服务`来得到设备的当前位置。要创建一个 `LocationListener`，然后向位置服务注册这个监听器。可以增加相应的规则，指定监听器多久得到一次变更通知。使用设备 GPS 时，需要在 AndroidManifest.xml 中为它增加一个授权。

- 要将一个活动绑定到一个服务，需要创建一个 `ServiceConnection`。覆盖 `onServiceConnected()` 方法来得到服务的一个引用。

- 使用 `bindService()` 方法绑定到服务。使用 `unbindService()` 方法与服务解除绑定。