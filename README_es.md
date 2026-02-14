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

Liquid es un tema de Typora inspirado en [Microsoft Fluent Design](https://www.microsoft.com/design/fluent/#/) y [Purple Theme](https://github.com/hliu202/typora-purple-theme). El repositorio actual incluye archivos listos para usar en `src/` (sin salida `dist/` separada).

## Estado actual

- Proyecto mantenido con cuatro variantes: `liquid`, `liquid-dark`, `liquid-ink`, `liquid-ink-dark`
- CSS fuente y fuentes tipográficas incluidos directamente en el repositorio
- Documentación y traducciones adaptadas al estado actual

## Características

- Estilo Fluent: degradados, esquinas redondeadas y acentos visuales
- Variantes Light / Dark / Ink / Ink Dark
- Estilos de CodeMirror personalizados para bloques de código
- Fuentes incluidas para texto serif, código monoespaciado y estilo manuscrito Ink

## Estructura del repositorio

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

## Instalación

1. Descarga `liquid.zip` desde [Releases](https://github.com/ruiyangzhou01/Liquid/releases) o clona este repositorio.
2. En Typora: **Preferences** → **Appearance** → **Open Theme Folder**.
3. Copia al directorio de temas:
   - `src/liquid.css`
   - `src/liquid-dark.css`
   - `src/liquid-ink.css`
   - `src/liquid-ink-dark.css`
   - `src/liquid/` (carpeta completa)
4. Reinicia Typora y selecciona una variante Liquid.
5. Abre `Demo.md` para previsualizar.

## Personalización

- Cambios rápidos: edita `liquid*.css` directamente en la carpeta de temas.
- Cambios profundos: edita módulos de `src/liquid/` (`main.css`, `color-*.css`, `font*.css`, `CodeMirror*.css`, `custom-*.css`).
- Overrides propios con CSS personalizado de Typora: <https://support.typora.io/Add-Custom-CSS/>.

## Solución de problemas

- **El tema no aparece**: confirma que los cuatro `liquid*.css` están en la raíz de la carpeta de temas.
- **Faltan fuentes o estilo Ink**: confirma que `liquid/` está junto a los CSS.
- **Sistemas sensibles a mayúsculas**: usa nombres exactos según CSS (`Inkfree.ttf`, `FZSJ-SGLDXMHJW.TTF`).

## Documentación

- [Documentación del tema Liquid](doc/Document_es.md)

## Licencia

[GPL-3.0 License](https://github.com/ruiyangzhou01/Liquid/blob/main/LICENSE) © ruiyangzhou01
