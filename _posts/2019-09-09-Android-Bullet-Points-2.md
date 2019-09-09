---
layout: post
title: Android 要点（二）
date: 2019-09-09 09:22:18 +0800
categories: Android
tags: Android 要点
---
- `Button` 元素用来增加按钮。
- `Spinner` 元素用来增加 Spinner。`Spinner` 是一个值下拉列表。
- 所有 GUI 组件都是某种类型的视图。它们都继承自 `View` 类。
- 使用以下代码增加字符串值数组：
    ``` XML
    <string-array name="array">
        <item>string1</item>
        ...
    </stirng-array>
    ```
- 使用以下代码在布局中引用 `string-array`：
    ``` XML
    "@array/array_name"
    ```
- 在布局中增加以下代码，单击按钮时就会让按钮调用一个方法：
    ``` XML
    android:onClick="clickMethod"
    ```
    活动中需要有一个相应的方法：
    ``` Java
    public void clickMethod(View view){

    }
    ```
- 会为你自动生成 `R.java`。利用这个文件，可以在 Java 代码中得到布局、GUI 组件、字符串和其他资源的引用。
- 使用 `findViewById()` 可以得到一个视图的引用。
- 使用 `setText()` 可以设置视图中的文本。
- 使用 `getSelectedItem()` 可以得到一个 `Spinner` 中所选择的列表项。
- 可以通过菜单 `File` → `New...` → `Java Class` 为 Android 工程增加一个定制类。