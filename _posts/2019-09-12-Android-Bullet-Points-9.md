---
layout: post
title: Android 开发 - 动作条
date: 2019-09-12 11:12:18 +0800
categories: Android
tags: Android 开发 要点 动作条
---
- 要为支持 API 11 或更高级别的应用增加动作条，可以应用某个 `Holo` 或 `Material` 主题。

- 要向支持 API 7 或更高级别的应用增加动作条，可以应用一个 `AppCompat` 主题并使用 `ActionBarActivity`。如果使用 `ActionBarActivity`，就必须使用 `AppCompat` 主题。

- `ActionBarActivity` 和 `AppCompat` 主题都在 `v7 AppCompat` 支持库中提供。

- `AndroidManifest.xml` 中的 `android:theme` 属性指定要应用哪个主题。

- 在样式资源文件中使用 `style` 元素定义样式。 `parent` 属性指定这个样式从哪里继承属性。

- 样式资源文件的默认文件夹是 `app/src/main/res/values`。如果希望在 API 21 上使用，要把样式资源文件放在 `app/src/main/res.valuse-v21` 文件夹中。

- 要为菜单资源文件增加菜单项为动作条增加动作项。

- 通过实现活动的 `onCreateOptionsMenu()` 方法，可以在菜单资源文件中为动作条增加动作项。

- 通过实现活动的 `onOptionsItemSelected()` 方法，可以指定单击动作项时要做些什么。

- 可以为动作条增加共享动作提供者来共享内容。要增加共享动作提供者，可以把它包含在菜单资源文件中。调用共享动作提供者的 `setShareIntent()` 方法传入一个意图，描述想要共享的内容。

- 可以为动作条增加一个向上按钮，在应用的层次结构中向上导航。层次结构在 `AndroidManifest.xml` 中指定。可以使用 `ActionBar setDisplayHomeAsUpEnabled()` 方法启用向上按钮。