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

Liquid is a Typora theme inspired by [Microsoft Fluent Design](https://www.microsoft.com/design/fluent/#/) and the [Purple Theme](https://github.com/hliu202/typora-purple-theme). It delivers a Windows 11-style reading and writing experience with gradients, mica-like surfaces, rounded rectangles, and bundled fonts. The theme ships four variants built from modular CSS.

## Features

- Fluent Design styling with gradients, mica, rounded rectangles, and colorful indicators
- Four variants: Light, Dark, Ink, and Ink Dark
- Customized CodeMirror styles for code blocks
- Bundled serif, handwriting, and monospace fonts

## Compatibility

- Windows 10 and Windows 11
- Typora desktop app
- Language coverage: English and Chinese (Source Han Serif CN). Ink modes also use Ink Free and FZSJ-SGLDXMHJW for handwriting.

## Screenshots

Liquid Theme aims to provide a modern Windows 11 visual experience in Typora. It uses UI elements such as gradients, mica material, and rounded rectangles. The theme supports English and Chinese, and it provides Light Mode, Dark Mode, Ink Mode, and Ink Dark Mode.

![preview](./media/theme/liquid/preview.png)

### Light Mode

![light-preview1](/media/theme/liquid/light-preview1.png)

![light-preview2](/media/theme/liquid/light-preview2.png)

![light-preview3](/media/theme/liquid/light-preview3.png)

### Dark Mode

![dark-preview1](/media/theme/liquid/dark-preview1.png)

![dark-preview2](/media/theme/liquid/dark-preview2.png)

![dark-preview3](/media/theme/liquid/dark-preview3.png)

### Ink Mode & Ink Dark Mode

If you use a 2-in-1 PC such as Microsoft Surface for study or writing, or you simply prefer handwritten fonts, Ink Mode provides a handwriting-style reading and writing experience in Typora.

![ink-preview1](/media/theme/liquid/ink-preview1.png)

![ink-preview2](/media/theme/liquid/ink-preview2.png)

![ink-preview3](/media/theme/liquid/ink-preview3.png)

## Installation

1. Download `liquid.zip` from the [Releases](https://github.com/ruiyangzhou01/Liquid/releases) page.
2. Open Typora settings. In **Preferences**, select **Appearance**, then click **Open Theme Folder**.
3. Unzip and copy `liquid.css`, `liquid-dark.css`, `liquid-ink.css`, `liquid-ink-dark.css`, and the `liquid/` font folder into the theme folder.
4. Restart Typora.
5. Select the Liquid theme from the **Themes** menu in Typora.
6. Open `Demo.md` from this repository (or the source code archive) to preview the local rendering.

### Ink mode fonts

Install `FZSJ-SGLDXMHJW.TTF` from `dist/liquid` (or from the release `liquid/` folder) to render Chinese characters in Ink modes. `Inkfree.ttf` provides the handwriting font for Latin text.

## Build from source

The build scripts are written for Windows paths.

1. Install Python 3.
2. Run `cd src/Deploy`.
3. Run `python CombineCSS.py` to combine `src/liquid*.css` into `dist/*.css`.
4. (Optional) Run `cd ../deploy` and `python CompressZip.py` to package `dist` as `liquid.zip`.

## Customization

- Add custom CSS via Typora (recommended): <https://support.typora.io/Add-Custom-CSS/>.
- Edit the compiled files in the theme folder (`dist/*.css` in this repository).
- For deeper changes, edit the modules in `src/liquid/` and rebuild. See the documentation below.

## Documentation

- [Liquid Theme Documentation](doc/Document.md)

## License

[GPL-3.0 License](https://github.com/ruiyangzhou01/Liquid/blob/main/LICENSE) © ruiyangzhou01
