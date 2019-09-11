---
layout: post
title: Android 开发 - 列表视图和适配器
date: 2019-09-10 13:56:18 +0800
categories: Android
tags: Android 开发 要点 列表 适配器
---
- 整理你的想法，将活动划分为顶级活动、类别活动和详细信息/编辑活动。使用类别活动从顶级活动导航到详细信息/编辑活动。

- 图像资源放在一个或多个 `drawable*` 文件夹中。可以在布局中使用 `@drawable/image_name` 引用这些图像资源。在活动代码中要用 `R.drawable.image_name` 访问这些资源。

- `ImageView` 包含一个图像。可以使用 `android:src` 设置图像源，另外可以使用 `android:contentDescription` 提供一个可访问的标签。Java 中的相应方法分别是 `setImageResource()` 和 `setContentDescription()`。

- `ListView` 显示一个列表中的列表项。

- 在布局中使用 `android:entries` 由 `strings.xml` 中定义的一个数组填充列表视图中的列表项。

- `ListActivity` 是一个 `Activity`，它提供了一个 `ListView`。可以使用 `getListView()` 得到这个 `ListView` 的引用。

- `ListActivity` 有自己的默认布局，不过可以把它替换为你自己的布局。

- `适配器`相当于 `AdapterView` 和一个`数据源`之间的一座桥。`ListView` 和 `Spinner` 是不同类型的 `AdapterView`。

- `ArrayAdapter` 是专门处理数组的适配器。

- 可以在布局代码中使用 `android:onClick` 处理 `Button` 单击事件。

- 可以实现 `onListItemClick()` 方法处理 `ListActivity` 中 `ListView` 上的单击事件。

- 处理其他单击事件时，要创建一个`监听器`并实现它的单击事件。