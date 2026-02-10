# Liquid Theme Documentation

[English](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document.md) • [中文](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_zh.md) • [Deutsch](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_de.md) • [Español](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_es.md) • [Français](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_fr.md) • [日本語](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_ja.md)

## Overview

Liquid is a Typora theme inspired by Microsoft Fluent Design. This document explains the file layout, build workflow, and customization options based on the current repository structure.

## File Structure

### Release Package (`liquid.zip`)

The release archive is produced from the `dist` folder and contains the compiled CSS plus fonts:

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

### Repository Layout

```text
Demo.md
README.md
README_*.md
LICENSE
media/                # preview images
font/                 # raw font sources
  JetBrainsMono-2.242/
  SourceHanSerifCN/
dist/                 # compiled CSS + font assets (release contents)
  liquid.css
  liquid-dark.css
  liquid-ink.css
  liquid-ink-dark.css
  liquid/
    *.ttf
    *.woff2
doc/                  # documentation translations
src/
  liquid.css           # entry point (light)
  liquid-dark.css      # entry point (dark)
  liquid-ink.css       # entry point (ink)
  liquid-ink-dark.css  # entry point (ink dark)
  liquid/              # CSS modules
    main.css
    color-light.css
    color-dark.css
    font.css
    font-ink.css
    CodeMirror.css
    CodeMirror-dark.css
    custom-ink.css
    custom-dark.css
  Deploy/CombineCSS.py # combines @import files into dist
  deploy/CompressZip.py # packages dist into liquid.zip
```

## Build From Source

The build scripts use Windows-style paths and are intended to run on Windows. CombineCSS.py lives in `src/Deploy` (capital D) and CompressZip.py in `src/deploy` (lowercase). On case-sensitive file systems, use the exact folder names.

1. Install Python 3.
2. Run `cd src/Deploy`.
3. Run `python CombineCSS.py` to recursively expand `@import` statements and write the compiled files into `dist/`.
4. (Optional) Run `cd ../deploy` and `python CompressZip.py` to create `liquid.zip` from the `dist` folder.

## CSS Module Map

The entry-point CSS files in `src/` import smaller modules under `src/liquid/`:

- `liquid.css`: light mode (imports `font.css`, `color-light.css`, `CodeMirror.css`, `main.css`).
- `liquid-dark.css`: dark mode (imports `font.css`, `color-dark.css`, `CodeMirror-dark.css`, `main.css`, `custom-dark.css`).
- `liquid-ink.css`: ink mode (imports `font-ink.css`, `color-light.css`, `CodeMirror.css`, `main.css`, `custom-ink.css`).
- `liquid-ink-dark.css`: ink dark mode (imports `font-ink.css`, `color-dark.css`, `CodeMirror-dark.css`, `main.css`, `custom-ink.css`, `custom-dark.css`).

Key modules:

- `main.css`: shared layout, typography, and component styling.
- `color-light.css` / `color-dark.css`: color variables for light and dark palettes.
- `font.css`: default fonts (Source Han Serif CN + JetBrains Mono).
- `font-ink.css`: handwriting fonts (Ink Free + FZSJ-SGLDXMHJW).
- `CodeMirror.css` / `CodeMirror-dark.css`: code block theme styles.
- `custom-ink.css`: ink-specific typography adjustments.
- `custom-dark.css`: dark-mode UI tweaks.

## Customization Options

### 1. Add Custom CSS (Recommended)

Use Typora’s custom CSS support to layer your own overrides without touching the theme files. Refer to <https://support.typora.io/Add-Custom-CSS/>.

### 2. Edit the Compiled Theme Files

After installing the theme, edit `liquid.css`, `liquid-dark.css`, `liquid-ink.css`, or `liquid-ink-dark.css` directly in your theme folder. Keep the `liquid/` font folder next to the CSS files so the `@font-face` declarations continue to resolve.

### 3. Edit the Source Modules

For deeper changes, edit the module files under `src/liquid/` and rebuild with `CombineCSS.py`. Typical adjustments include:

- Colors: `color-light.css` and `color-dark.css`
- Fonts: `font.css` and `font-ink.css`
- Code blocks: `CodeMirror.css` and `CodeMirror-dark.css`
- Ink/dark tweaks: `custom-ink.css` and `custom-dark.css`
- Layout and typography: `main.css`

## Font Notes

Ink modes rely on `Inkfree.ttf` for Latin handwriting and `FZSJ-SGLDXMHJW.TTF` for Chinese handwriting. Install the `FZSJ-SGLDXMHJW.TTF` font locally if you need Chinese characters in Ink modes.
