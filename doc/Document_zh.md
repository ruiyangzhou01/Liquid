# Liquid 主题文档

[English](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document.md) • [中文](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_zh.md) • [Deutsch](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_de.md) • [Español](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_es.md) • [Français](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_fr.md) • [日本語](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_ja.md)

## 概述

Liquid 是一个灵感来自 Microsoft Fluent Design 的 Typora 主题。本文档基于当前仓库结构，说明文件布局、构建流程与自定义方式。

## 文件结构

### 发布包（`liquid.zip`）

发布包由 `dist` 目录生成，包含编译后的 CSS 与字体：

```text
liquid.css
liquid-dark.css
liquid-ink.css
liquid-ink-dark.css
liquid/
  JetBrainsMono-Bold.woff2
  JetBrainsMono-Regular.woff2
  SourceHanSerifCN-Bold.ttf
  SourceHanSerifCN-Regular.ttf
  Inkfree.ttf
  FZSJ-SGLDXMHJW.TTF
```

### 仓库结构

```text
Demo.md
README.md
README_*.md
LICENSE
media/                # 预览图片
font/                 # 字体源文件
  JetBrainsMono-2.242/
  SourceHanSerifCN/
dist/                 # 编译后的 CSS 与字体资源（发布包内容）
  liquid.css
  liquid-dark.css
  liquid-ink.css
  liquid-ink-dark.css
  liquid/
    *.ttf
    *.woff2
doc/                  # 文档翻译
src/
  liquid.css           # 入口文件（light）
  liquid-dark.css      # 入口文件（dark）
  liquid-ink.css       # 入口文件（ink）
  liquid-ink-dark.css  # 入口文件（ink dark）
  liquid/              # CSS 模块
    main.css
    color-light.css
    color-dark.css
    font.css
    font-ink.css
    CodeMirror.css
    CodeMirror-dark.css
    custom-ink.css
    custom-dark.css
  Deploy/CombineCSS.py # 合并 @import 输出到 dist
  deploy/CompressZip.py # 将 dist 打包为 liquid.zip
```

## 从源码构建

构建脚本使用 Windows 风格路径，建议在 Windows 上执行。CombineCSS.py 位于 `src/Deploy`（大写 D），CompressZip.py 位于 `src/deploy`（小写 d）。在区分大小写的文件系统中请使用准确的目录名。

1. 安装 Python 3。
2. 运行 `cd src/Deploy`。
3. 运行 `python CombineCSS.py`，递归展开 `@import` 并输出到 `dist/`。
4. （可选）运行 `cd ../deploy` 和 `python CompressZip.py`，从 `dist` 生成 `liquid.zip`。

## CSS 模块说明

`src/` 下的入口 CSS 文件会引入 `src/liquid/` 中的模块：

- `liquid.css`：light 模式（引入 `font.css`、`color-light.css`、`CodeMirror.css`、`main.css`）。
- `liquid-dark.css`：dark 模式（引入 `font.css`、`color-dark.css`、`CodeMirror-dark.css`、`main.css`、`custom-dark.css`）。
- `liquid-ink.css`：ink 模式（引入 `font-ink.css`、`color-light.css`、`CodeMirror.css`、`main.css`、`custom-ink.css`）。
- `liquid-ink-dark.css`：ink dark 模式（引入 `font-ink.css`、`color-dark.css`、`CodeMirror-dark.css`、`main.css`、`custom-ink.css`、`custom-dark.css`）。

主要模块说明：

- `main.css`：通用布局、排版与组件样式。
- `color-light.css` / `color-dark.css`：浅色/深色调色板变量。
- `font.css`：默认字体（Source Han Serif CN + JetBrains Mono）。
- `font-ink.css`：手写字体（Ink Free + FZSJ-SGLDXMHJW）。
- `CodeMirror.css` / `CodeMirror-dark.css`：代码块样式。
- `custom-ink.css`：Ink 模式的排版调整。
- `custom-dark.css`：Dark 模式的 UI 调整。

## 自定义方式

### 1. 添加自定义 CSS（推荐）

使用 Typora 的自定义 CSS 功能为主题添加覆盖样式，详见 <https://support.typora.io/Add-Custom-CSS/>。

### 2. 编辑编译后的主题文件

安装主题后，直接编辑主题目录中的 `liquid.css`、`liquid-dark.css`、`liquid-ink.css` 或 `liquid-ink-dark.css`。请确保 `liquid/` 字体目录与 CSS 文件同级，以便 `@font-face` 正确加载。

### 3. 编辑源码模块

如需更深度的定制，请修改 `src/liquid/` 中的模块并使用 `CombineCSS.py` 重新构建。常见修改位置：

- 颜色：`color-light.css` 与 `color-dark.css`
- 字体：`font.css` 与 `font-ink.css`
- 代码块：`CodeMirror.css` 与 `CodeMirror-dark.css`
- Ink/Dark 调整：`custom-ink.css` 与 `custom-dark.css`
- 布局与排版：`main.css`

## 字体说明

Ink 模式依赖 `Inkfree`（拉丁文字）与 `FZSJ-SGLDXMHJW`（中文手写）。字体已通过 `@font-face` 打包，通常不需要系统安装。在区分大小写的文件系统中，请确认 `liquid/` 目录的文件名与 CSS 引用一致（`inkfree.ttf` 与 `FZSJ-SGLDXMHJW.ttf`），必要时重命名文件或修改 CSS。
