---
layout: post
title: Android 开发 - 材料设计
date: 2019-09-18 09:26:18 +0800
categories: Android
tags: Android 开发 要点 材料设计
---
- `卡片视图`和`回收视图`有自己的支持库。

- 可以使用 `CardView` 元素为布局增加卡片视图。

- 可以使用 `cardCornerRadius` 属性为卡片视图指定圆角。这需要命名空间 "http://schemas.android.com/apk/res-auto"。

- 回收视图使用的适配器是 `RecyclerView.Adapter` 的子类。

- 创建你自己的 `RecyclerView.Adapter` 时，必须定义 `ViewHolder`，并实现 `onCreateViewHolder()`、`onBindViewHolder()` 和 `getItemCount()` 方法。

- 使用 `RecyclerView` 元素为布局增加回收视图。使用 `android:scrollbars` 属性为它指定滚动条。

- 要用一个`布局管理器`指定回收视图中的数据项如何组织。 `LinearLayoutManager` 会用一个线性列表组织数据项，`GridLayoutManager` 在一个网格中组织数据项，`StaggeredGridLayoutManager` 则在一个交错网格中组织数据项。