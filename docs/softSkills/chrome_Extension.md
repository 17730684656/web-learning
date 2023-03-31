---
title: manifest.json 配置详解
nav:
  title: 前端软技能
  order: 1
group:
  title: chrome 插件开发手册
  order: 3
---

# manifest.json 配置详解

<span style="color: red">它必须位于扩展程序的根目录，也是必须存在的一个文件。</span>

`manifest.json` 的作用是：记录重要的元数据，定义资源，声明权限，并且标识哪些文件在后台和页面上运行。

```json
{
  "manifest_version": 3, //  chrome 扩展的版本  最新的是 v3.  v2版本正在初步不支持
  "name": "extension name", //  chrome 插件的名字
  "description": "extension description", //  chrome 插件的简介
  "version": "1.0" // 该插件的版本号
}
```
