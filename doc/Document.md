# Liquid Theme Documentation

[English](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document.md) • [中文](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_zh.md) • [Deutsch](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_de.md) • [Español](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_es.md) • [Français](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_fr.md) • [日本語](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_ja.md)

## Overview

Liquid is a Typora theme inspired by Microsoft Fluent Design. The current repository is source-first: theme entry files and modules are kept directly under `src/`.

## Repository layout

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

## Theme variants

- `liquid.css`: light mode
- `liquid-dark.css`: dark mode
- `liquid-ink.css`: ink mode
- `liquid-ink-dark.css`: ink dark mode

## How to install

1. Open Typora theme folder from **Preferences → Appearance → Open Theme Folder**.
2. Copy the four `src/liquid*.css` files into that folder.
3. Copy the full `src/liquid/` folder next to the CSS files.
4. Restart Typora and select a Liquid variant.

## Module map

Entry files import modules from `src/liquid/`:

- Typography/layout: `main.css`
- Color tokens: `color-light.css`, `color-dark.css`
- Font stacks: `font.css`, `font-ink.css`
- Code block styles: `CodeMirror.css`, `CodeMirror-dark.css`
- Variant overrides: `custom-ink.css`, `custom-dark.css`

## Customization workflow

1. Start with direct CSS edits in installed `liquid*.css` if you only need quick adjustments.
2. For structural changes, edit module files in `src/liquid/`.
3. Keep your personal overrides in Typora custom CSS whenever possible to simplify updates.

## Font notes

- Ink variants use `Inkfree` for Latin handwriting-like text and `FZSJ-SGLDXMHJW` for Chinese handwriting style.
- Fonts are loaded via `@font-face` from the local `liquid/` folder.
- On case-sensitive file systems, ensure font filename case matches CSS references.

## Troubleshooting

- Theme not listed: verify all four `liquid*.css` files are in the theme folder root.
- Font not applied: verify `liquid/` folder is copied beside the CSS files.
- Styles not changing: disable custom CSS temporarily to rule out selector conflicts.
