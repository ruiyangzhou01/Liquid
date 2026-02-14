---
layout: theme
title: Liquid
category: theme
homepage: https://github.com/ruiyangzhou01/Liquid
download: https://github.com/ruiyangzhou01/Liquid/releases
built-in: false
author: ruiyangzhou01
thumbnail: liquid.png
typora-root-url: ../../
typora-copy-images-to: ../../media/theme/Liquid
---

# Liquid

<p>
    <img alt="release" src="https://img.shields.io/github/v/release/ruiyangzhou01/liquid?&color=blue&logo=hack-the-box"/>
    <img alt="downloads" src="https://img.shields.io/github/downloads/ruiyangzhou01/liquid/total?logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABEAAAAVCAYAAACg/AXsAAAAAXNSR0IArs4c6QAAAX1JREFUOE/llLEuBGEUhb+zIaHR8gYapUQUig1RaEg0Wo3GC4hOoaDXKVQ6UXgAoVGIaBRGYiMSXkBDMEf+mdmZf3bWegBTTe5/77nnnnv+Xwz4bE8AF5ImB+XpD5Ap4OQ/gtjeABaA4aCRgUKsb2Ab2CujxWEK7y04lnQm2zuYtW5VLnQJcydp1XYSI0c5IXE3gFwDY7XiikoFUq7RGMU9b+XUSYhEI8T/OUickyXG2XSU2kkeizv8Pk6FUeZ0ZKdJRc98o60h6dT2jeGp1dUEXiW1be8Dy5FJA4iTumuzDvPAC3AqacX2laRZ27PAUY/L+4xTjbuIeFYuAP70HEMcVsfF+CZn0l9U84GWRqRH28FDB801Z5w6xXZqavdYhXNMu9xgv+00jBRvqlnQ26Bg0hW2UVCwi+MNwpkumSb3YMUu/Buv5trHAHIJjAfPxn4pr2CPmn3MdhVA1oGtX5Sv34fmM/gFbGY33vZ0CjMtGB30XMZnKby14FzSww+Jf/H06Zp5zAAAAABJRU5ErkJggg=="/>
    <img alt="stars" src="https://img.shields.io/github/stars/ruiyangzhou01/liquid?style=flat&logo=github&color=yellow"/>
    <img alt="forks" src="https://img.shields.io/github/forks/ruiyangzhou01/Liquid"/>
</p>

<p>
    <img alt="maintenance" src="https://img.shields.io/badge/Maintained%3F-yes-green/ruiyangzhou01/Liquid"/>
    <img alt="issues" src="https://img.shields.io/github/issues/ruiyangzhou01/liquid"/>
    <img alt="issues closed" src="https://img.shields.io/github/issues-closed/ruiyangzhou01/liquid"/>
</p>

[English](https://github.com/ruiyangzhou01/Liquid/blob/main/README.md) • [中文](https://github.com/ruiyangzhou01/Liquid/blob/main/README_zh.md) • [Deutsch](https://github.com/ruiyangzhou01/Liquid/blob/main/README_de.md) • [Español](https://github.com/ruiyangzhou01/Liquid/blob/main/README_es.md) • [Français](https://github.com/ruiyangzhou01/Liquid/blob/main/README_fr.md) • [日本語](https://github.com/ruiyangzhou01/Liquid/blob/main/README_ja.md)

Liquid 是一个受 [Microsoft Fluent Design](https://www.microsoft.com/design/fluent/#/) 与 [Purple Theme](https://github.com/hliu202/typora-purple-theme) 启发的 Typora 主题。当前仓库直接提供 `src/` 下可用的主题源码（不再有独立 `dist/` 构建产物）。

## 当前状态

- 持续维护，提供四个模式：`liquid`、`liquid-dark`、`liquid-ink`、`liquid-ink-dark`
- 源码 CSS 与字体文件直接在仓库中维护
- 文档与翻译已按当前仓库结构更新

## 特性

- Fluent 风格视觉：渐变、圆角、强调色指示、类云母质感
- Light / Dark / Ink / Ink Dark 四种模式
- 定制 CodeMirror 代码块样式
- 内置衬线、等宽和 Ink 手写风格字体

## 仓库结构

```text
src/
  liquid.css
  liquid-dark.css
  liquid-ink.css
  liquid-ink-dark.css
  liquid/
    *.css
    *.ttf
    *.woff2
Demo.md
README*.md
doc/Document*.md
media/
assets/
```

## 安装

1. 从 [Releases](https://github.com/ruiyangzhou01/Liquid/releases) 下载 `liquid.zip`，或直接克隆仓库。
2. 打开 Typora → **偏好设置** → **外观** → **打开主题文件夹**。
3. 将以下文件复制到 Typora 主题目录：
   - `src/liquid.css`
   - `src/liquid-dark.css`
   - `src/liquid-ink.css`
   - `src/liquid-ink-dark.css`
   - `src/liquid/`（整个目录）
4. 重启 Typora，在 **主题** 菜单中选择 Liquid 模式。
5. 打开 `Demo.md` 预览效果。

## 自定义

- 快速调整：直接编辑主题目录中的 `liquid*.css`。
- 深度定制：编辑 `src/liquid/` 模块（`main.css`、`color-*.css`、`font*.css`、`CodeMirror*.css`、`custom-*.css`）。
- 通过 Typora 自定义 CSS 添加覆盖层：<https://support.typora.io/Add-Custom-CSS/>。

## 故障排查

- **Typora 中看不到主题**：确认四个 `liquid*.css` 已复制到主题目录根路径。
- **字体或 Ink 效果缺失**：确认 `liquid/` 目录与 CSS 文件处于同级。
- **区分大小写系统出现缺字**：检查字体文件名大小写与 CSS 引用一致（如 `Inkfree.ttf`、`FZSJ-SGLDXMHJW.TTF`）。

## 文档

- [Liquid 主题文档](doc/Document_zh.md)

## 许可证

[GPL-3.0 License](https://github.com/ruiyangzhou01/Liquid/blob/main/LICENSE) © ruiyangzhou01
