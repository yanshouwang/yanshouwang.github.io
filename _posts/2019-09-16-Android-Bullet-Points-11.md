---
layout: post
title: Android 开发 - SQLite 数据库
date: 2019-09-16 13:11:18 +0800
categories: Android
tags: Android 开发 要点 SQLite 数据库
---
- Android 使用 `SQLite` 作为它的后备数据库持久存储数据。

- 可以利用 `SQLiteDatabase` 类访问 SQLite 数据库。

- `SQLite 帮助器`允许你创建和管理 SQLite 数据库。创建 SQLite 帮助器时要扩展 `SQLiteOpenHelper` 类。

- 必须实现 `SQLiteOpenHelper` 的 `OnCreate()` 和 `onUpgrade()` 方法。

- 第一次要访问数据库时会创建数据库。要为数据库指定一个名字和版本号，版本号从 1 开始。如果没有为数据库指定名字，就会在内存中创建这个数据库。

- 第一次创建数据库时会调用 `onCreate()` 方法。

- 数据库需要升级时要调用 `onUpgrade()` 方法。

- 可以使用 `SQLiteDatabase` 的 `execSQL(String)` 方法执行 SQL 命令。

- 可以使用 `insert()` 方法为表增加记录。

- 可以使用 `update()` 方法更新记录。

- 可以使用 `delete()` 方法从表删除记录。