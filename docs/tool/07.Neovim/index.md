---
title: Neovim
date: 2024-08-20 11:13:26
order:
---

## Neovim 是什么

## 安装

## 配置

所有 Vim 命令都可以在 Neovim 中使用，Neovim 的配置文件格式也与 Vim 相同。不过，`vimrc` 在 Neovim 中不会自动加载。Neovim 的配置文件，按照 Bek Brace 的教程，放在 `C:\Users\Alowr\AppData\Local\nvim\` 目录中。

In Vim, when you run the following commands, you get:

```vim
:echo $VIM           " C:\Program Files\Vim
:echo $HOME          " C:\Users\Alowr
:echo $VIMRUNTIME    " C:\Program Files\Vim\vim91
```

In Neovim, you have the following instead:

```nvim
:echo $VIM           " C:\Program Files\Neovim\share\nvim
:echo $HOME          " C:\Users\Alowr
:echo $VIMRUNTIME    " C:\Program Files\Neovim\share\nvim\runtime
```

The following steps are just a follow through from this video [Windows11 里定制个性 PowerShell + Neovim 全程音乐不废话 ！](https://www.bilibili.com/video/BV1Gz421D7Qr/)

1. 创建 `C:\Users\Alowr\AppData\Local\nvim\init.vim` 配置文件，复制并粘贴 Bek Brace 的配置文件，作为配置的起点
2. 在 Windows PowerShell 内安装插件管理器 vim-plug
   ```ps
   iwr -useb https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim |`
       ni "$(@($env:XDG_DATA_HOME, $env:LOCALAPPDATA)[$null -eq $env:XDG_DATA_HOME])/nvim-data/site/autoload/plug.vim" -Force
   ```
3. 在 Neovim 内运行 `:PlugInstall` 以安装配置文件内的各种插件
4. 安装完成后重启 Neovim，很多插件已经可以使用
5. Prettier formatter for coc.nvim, run vim command:
   ```vim
   :CocInstall coc-prettier
   ```
6. To install prettier in your project and pin its version as recommended, run:
   ```ps
   pnpm install prettier -D --save-exact
   ```
7. Configuration on coc.nvim: open settings file with:

   ```
   :CocConfig
   ```

   Add:

   ```json
   {
     "coc.preferences.formatOnSaveFiletypes": ["css", "markdown"],
   ```

到这一步，Markdown 文档在保存时已经可以自动格式化了。

另外，这个视频的另外一个重要之外，是教你配置 PowerShell 的历史命令菜单，好用。

## Other thoughts

- PowerShell 环境变量，`Get-ChildItem env:*`
