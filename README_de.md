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

Liquid ist ein Typora-Theme, inspiriert von [Microsoft Fluent Design](https://www.microsoft.com/design/fluent/#/) und dem [Purple Theme](https://github.com/hliu202/typora-purple-theme). Dieses Repository enthält direkt nutzbare Theme-Dateien unter `src/` (kein separates `dist/`).

## Aktueller Stand

- Aktiv gepflegt, mit vier Varianten: `liquid`, `liquid-dark`, `liquid-ink`, `liquid-ink-dark`
- Quell-CSS und Schriften liegen direkt im Repository
- Dokumentation und Übersetzungen entsprechen der aktuellen Struktur

## Funktionen

- Fluent-ähnliches Design mit Verläufen, runden Ecken und Akzentflächen
- Light / Dark / Ink / Ink Dark
- Angepasste CodeMirror-Stile für Codeblöcke
- Mitgelieferte Serif-, Monospace- und Ink-Schriften

## Repository-Struktur

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

1. `liquid.zip` von [Releases](https://github.com/ruiyangzhou01/Liquid/releases) laden oder Repository klonen.
2. In Typora: **Preferences** → **Appearance** → **Open Theme Folder**.
3. In den Theme-Ordner kopieren:
   - `src/liquid.css`
   - `src/liquid-dark.css`
   - `src/liquid-ink.css`
   - `src/liquid-ink-dark.css`
   - `src/liquid/` (kompletter Ordner)
4. Typora neu starten und ein Liquid-Theme auswählen.
5. `Demo.md` zur Vorschau öffnen.

## Anpassung

- Schnell anpassen: installierte `liquid*.css` direkt bearbeiten.
- Tiefer anpassen: Module unter `src/liquid/` bearbeiten (`main.css`, `color-*.css`, `font*.css`, `CodeMirror*.css`, `custom-*.css`).
- Eigene Overrides über Typora Custom CSS: <https://support.typora.io/Add-Custom-CSS/>.

## Fehlerbehebung

- **Theme erscheint nicht**: prüfen, ob alle vier `liquid*.css` im Theme-Ordner liegen.
- **Ink/Schrift fehlt**: prüfen, ob `liquid/` neben den CSS-Dateien liegt.
- **Dateisensitive Systeme**: Dateinamen exakt wie in CSS referenziert verwenden (`Inkfree.ttf`, `FZSJ-SGLDXMHJW.TTF`).

## Dokumentation

- [Liquid-Theme-Dokumentation](doc/Document_de.md)

## Lizenz

[GPL-3.0 License](https://github.com/ruiyangzhou01/Liquid/blob/main/LICENSE) © ruiyangzhou01
