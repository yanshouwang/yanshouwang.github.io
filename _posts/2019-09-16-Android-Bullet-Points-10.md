---
layout: post
title: Android 开发 - 导航抽屉
date: 2019-09-16 11:12:18 +0800
categories: Android
tags: Android 开发 要点 导航抽屉
---
- 使用 `DrawerLayout` 创建一个带导航抽屉的活动。可以使用这个抽屉导航到应用的主要导航项目。

- 如果使用一个动作条，可以使用 `ActionBarDrawerToggle` 作为 `DrawerListener`，以响应抽屉的打开和关闭，另外会为动作条增加一个图标来打开和关闭抽屉。

- 要在运行时改变动作条中的动作项，可以调用 `invalidateOptionsMenu()`，并在活动的 `onPrepareOptionsMenu()` 方法中指定如何改变。

- 可以实现 `FragmentManager.OnBackStackChangedListener()` 响应后退堆栈的变化。

- 片段管理器的 `findFragmentByTag()` 方法会搜索有指定标记的片段。