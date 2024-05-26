---
title: Soundfreaq
date: 2024-05-19 12:10:15
order: 1
---

# {{ $frontmatter.title }}

Ideally, this page should be generated automatically, with names and links to each of the sub-folders.

经过测试，在当前 clone 下来的项目中，直接添加来自 Vdoing 项目的一级文件夹之后：

1. 每个级别的文件夹内，都需要一一手动添加一个 index.md 文件
2. config/nav/ 文件夹内，添加配置文件
3. config/sidebar/ 文件夹内，添加配置文件
4. config/nav.ts 文件内，添加配置项
5. config/sidebar.ts 文件内，添加配置项

这样配置之后，在导航栏可以添加一个新增一级文件夹的入口。

如果不需要更改导航栏，只需配置第 3、5 项
