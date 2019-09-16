---
layout: post
title: Android 开发 - 游标与 AsyncTask
date: 2019-09-16 13:11:18 +0800
categories: Android
tags: Android 开发 要点 游标 AsyncTask Cursor
---
- 可以利用游标读写数据库。

- 可以调用 `SQLiteDatabase` 的 `query()` 方法创建游标。在底层，这会建立一个 `SQL SELECT` 语句。

- `getWritableDatabase()` 方法返回一个 `SQLiteDatabase` 对象，允许读写数据库。

- `getReadableDatabase()` 方法返回一个 `SQLiteDatabase` 对象，允许以只读方式访问数据库。也可能可以读写数据库，不过不能保证这一点。

- 可以使用 `moveTo*()` 方法导航游标。

- 可以使用 `get*()` 方法从游标获取值。

- 使用完游标和数据库之后要关闭游标和数据库连接。

- `CursorAdapter` 是一个使用游标的适配器。可以利用 `SimpleCursorAdapter` 用游标返回的值填充 `ListView`。

- 要适当的设计应用，把有用的内容放在顶层活动中。

- `CursorAdapter` 的 `changeCursor()` 方法把游标适配器当前使用的游标替换为你提供的一个新游标。然后关闭原来的游标。

- 可以使用 `AsyncTask` 在后台线程中允许数据库代码。