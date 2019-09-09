---
layout: post
title: Android 开发 - 多个活动和意图
date: 2019-09-09 11:27:18 +0800
categories: Android
tags: Android 开发 要点 活动 意图
---
- 任务是两个或多个串在一起的活动。

- `EditText` 元素定义一个可编辑的文本域，用来输入文本。它继承自 `View` 类。

- 可以选择 `File` → `New...` → `Activity` 在 Android Studio 中增加一个新活动。

- 所创建的活动必须在 `AndroidManifest.xml` 中有相应的一个记录。

- `Intent` 是 Android 组件相互通信所使用的消息类型。

- 显式意图显式地指定这个意图的目标组件。可以使用以下代码创建显式意图：

    ``` Java
    Intent intent = new Intent(this, Target.class); 
    ```

- 要启动一个活动，可以调用 `startActivity(intent)`。如果没有找到匹配的活动，会抛出一个 `ActivityNotFoundException`。

- 可以使用 `putExtra()` 方法为意图增加额外的信息。

- 可以使用 `getIntent()` 方法获取启动这个活动的意图。

- 可以使用 `get*Extra()` 方法获取与意图关联的额外信息。`getStringExtra()` 会获取一个 `String`，`getIntExtra()` 会获取一个 `int`，依此类推。

- `Action` 描述活动可以完成的一个标准可操作的动作。例如，要发送一个消息，可以使用 `Intent.ACTION_SEND`。

- 要创建指定一个动作的隐式意图，可以使用以下代码：

    ``` Java
    Intent intent = new Intent(action);
    ```

- 要描述意图中的数据类型，可以使用 `setType()` 方法。

- Android 根据命名组件、动作、数据类型和意图中指定的类别解析意图。它将意图的内容与各个应用的 `AndroidManifest.xml` 中的意图过滤器进行比较。如果一个活动要接收隐式意图，它的类别必须是 `DEFAULT`。

- `createChooser()` 方法允许覆盖默认的 Android 活动选择器对话框。它允许为这个对话框指定一个标题，而且不提供选项让用户设置默认活动。如果没有活动能接收传入的意图，它会显示一个消息。`createChooser()` 方法返回一个 `Intent`。

- 可以使用 `getString(R.string.stringname)` 获取字符串资源的值。