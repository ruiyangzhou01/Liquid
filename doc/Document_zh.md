# Liquid 主题文档

[English](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document.md) • [中文](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_zh.md) • [Deutsch](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_de.md) • [Español](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_es.md) • [Français](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_fr.md) • [日本語](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_ja.md)

## 概述

Liquid 是一个受 Microsoft Fluent Design 启发的 Typora 主题。当前仓库采用源码直出结构：主题入口文件与模块都位于 `src/`。

## 仓库结构

```text
src/
  liquid.css
  liquid-dark.css
  liquid-ink.css
  liquid-ink-dark.css
  liquid/
    main.css
    color-light.css
    color-dark.css
    font.css
    font-ink.css
    CodeMirror.css
    CodeMirror-dark.css
    custom-ink.css
    custom-dark.css
    Inkfree.ttf
    FZSJ-SGLDXMHJW.TTF
    SourceHanSerifCN-*.ttf
    JetBrainsMono-*.woff2
Demo.md
doc/Document*.md
README*.md
media/
assets/
```

## 主题模式

- `liquid.css`：浅色模式
- `liquid-dark.css`：深色模式
- `liquid-ink.css`：Ink 模式
- `liquid-ink-dark.css`：Ink 深色模式

## 安装方法

1. 在 Typora 中打开 **偏好设置 → 外观 → 打开主题文件夹**。
2. 将 `src/liquid*.css` 四个文件复制到主题目录。
3. 将完整 `src/liquid/` 目录复制到与 CSS 同级位置。
4. 重启 Typora 并选择 Liquid 主题。

## 模块说明

入口文件会引入 `src/liquid/` 下模块：

- 布局与排版：`main.css`
- 颜色变量：`color-light.css`、`color-dark.css`
- 字体栈：`font.css`、`font-ink.css`
- 代码块样式：`CodeMirror.css`、`CodeMirror-dark.css`
- 模式修饰：`custom-ink.css`、`custom-dark.css`

## 自定义流程

1. 小改动：直接编辑已安装的 `liquid*.css`。
2. 大改动：编辑 `src/liquid/` 模块文件。
3. 建议将个人偏好放在 Typora 自定义 CSS，便于后续升级。

## 字体说明

- Ink 模式中，`Inkfree` 用于拉丁文字手写风格，`FZSJ-SGLDXMHJW` 用于中文手写风格。
- 字体通过本地 `liquid/` 目录中的 `@font-face` 加载。
- 在区分大小写的文件系统上，请确保字体文件名与 CSS 引用大小写完全一致。

## 故障排查

- 主题未显示：检查四个 `liquid*.css` 是否位于主题目录根路径。
- 字体未生效：检查 `liquid/` 是否与 CSS 同级。
- 样式没有变化：临时关闭自定义 CSS，排查选择器覆盖冲突。
