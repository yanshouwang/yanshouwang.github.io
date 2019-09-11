---
layout: post
title: Android 开发 - 用户界面
date: 2019-09-10 09:14:18 +0800
categories: Android
tags: Android 开发 要点 界面
---
- `GUI 组件`是各种不同类型的视图。它们都是 `android.view.View` 类的子类。

- 所有布局都是 `android.view.ViewGroup` 类的子类。`视图组`是一种可以包含多个视图的视图类型。

- 布局 XML 文件会转换成一个包含视图层次树的 `ViewGroup`。

- `相对布局`可以相对于其他视图显示子视图，或者相对于父布局显示子视图。

- `线性布局`会水平或垂直显示视图。可以使用 `android:Orientation` 属性指定方向。

- `网格布局`将屏幕划分为一个单元格网格，可以指定各个视图占据哪个（或哪些）单元格。可以使用 `android:columnCount` 指定要有多少列。另外可以使用 `android:layout_row` 和 `android:layout_column` 指定希望各个视图出现在哪个单元格上。可以使用 `android:layout_columnSpan` 指定视图跨多少列。

- 可以使用 `android:padding*` 属性指定一个视图周围有多大的边距。

- 如果希望一个视图在布局中占据额外的空间，可以在线性布局中使用 `android:layout_weight`。

- `android:layout_gravity` 允许你指定希望视图出现在可用空间的哪个位置。

- `android:gravity` 允许你指定希望视图的内容出现在视图中的什么位置。

- `ToggleButton` 定义了一个开关按钮，可以单击这个按钮，在两个状态间做出选择。

- `Switch` 定义了一个开关控件，它与开关按钮的行为类似。使用这个控件时，至少要求使用 API 14 或更高等级的 SDK。

- `CheckBox` 定义一个复选框。

- 要定义一组单选钮，首先使用 `RadioGroup` 定义单选钮组。然后在这个单选钮组中用 `RadioButton` 增加各个单选钮。

- 使用 `ImageView` 显示图像。

- `ImageButton` 定义一个只有图像无文本的按钮。

- 可以使用 `ScrollView` 或 `HorizontalScrollView` 增加滚动条。

- `Toast` 是一个弹出式消息。