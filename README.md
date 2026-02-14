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

Liquid is a Typora theme inspired by [Microsoft Fluent Design](https://www.microsoft.com/design/fluent/#/) and the [Purple Theme](https://github.com/hliu202/typora-purple-theme). The current repository ships source-ready theme files under `src/` (no separate `dist/` build output).

## Current status

- Maintained theme with four variants: `liquid`, `liquid-dark`, `liquid-ink`, `liquid-ink-dark`
- Source CSS and bundled fonts are versioned directly in this repository
- Documentation and translations are aligned with the current source layout

## Features

- Fluent-style visuals: gradients, rounded corners, accent indicators, and mica-inspired surfaces
- Light / Dark / Ink / Ink Dark variants
- Customized CodeMirror styling for code blocks
- Bundled fonts for serif text, monospaced code, and handwriting-like Ink modes

## Repository layout

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

## Installation

1. Download `liquid.zip` from [Releases](https://github.com/ruiyangzhou01/Liquid/releases) or clone this repository.
2. Open Typora → **Preferences** → **Appearance** → **Open Theme Folder**.
3. Copy these files into the Typora theme folder:
   - `src/liquid.css`
   - `src/liquid-dark.css`
   - `src/liquid-ink.css`
   - `src/liquid-ink-dark.css`
   - `src/liquid/` (entire folder)
4. Restart Typora and select a Liquid variant from **Themes**.
5. Open `Demo.md` to preview the theme.

## Customization

- Quick tweaks: edit installed `liquid*.css` files directly in your Typora theme folder.
- Deep customization: edit module files in `src/liquid/` (`main.css`, `color-*.css`, `font*.css`, `CodeMirror*.css`, `custom-*.css`).
- Add your own override stylesheet using Typora custom CSS: <https://support.typora.io/Add-Custom-CSS/>.

## Troubleshooting

- **Theme not visible in Typora**: confirm all four `liquid*.css` files are copied into the theme folder root.
- **Fonts or Ink style missing**: confirm the `liquid/` folder is copied next to the CSS files.
- **Glyph issues on case-sensitive systems**: verify filename case matches CSS references (for example `Inkfree.ttf` and `FZSJ-SGLDXMHJW.TTF`).

## Documentation

- [Liquid Theme Documentation](doc/Document.md)

## License

[GPL-3.0 License](https://github.com/ruiyangzhou01/Liquid/blob/main/LICENSE) © ruiyangzhou01
