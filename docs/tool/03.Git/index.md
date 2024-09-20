---
title: Git
date: 2024-05-15 23:54:05
order:
---

## Git 是什么

版本控制工具

## git 命令

`git remote` 命令用于用于管理 Git 仓库中的远程仓库。

`git remote` 命令提供了一些用于查看、添加、重命名和删除远程仓库的功能。

以下是 `git remote` 命令的常见用法：

- `git remote`：列出当前仓库中已配置的远程仓库
- `git remote -v`：列出当前仓库中已配置的远程仓库，并显示它们的 URL
- `git remote add <remote_name> <remote_url>`：添加一个新的远程仓库。指定一个远程仓库的名称和 URL，将其添加到当前仓库中
- `git remote rename <old_name> <new_name>`：将已配置的远程仓库重命名
- `git remote remove <remote_name>`：从当前仓库中删除指定的远程仓库
- `git remote set-url <remote_name> <new_url>`：修改指定远程仓库的 URL
- `git remote show <remote_name>`：显示指定远程仓库的详细信息，包括 URL 和跟踪分支

## Git 入门相关文章推荐

- [Git 原理入门 - 阮一峰](https://www.ruanyifeng.com/blog/2018/10/git-internals.html)
- [常用 Git 命令清单 - 阮一峰](https://www.ruanyifeng.com/blog/2015/12/git-cheat-sheet.html)
