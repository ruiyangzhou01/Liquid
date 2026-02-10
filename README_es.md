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

Liquid es un tema de Typora inspirado en [Microsoft Fluent Design](https://www.microsoft.com/design/fluent/#/) y en [Purple Theme](https://github.com/hliu202/typora-purple-theme). Ofrece una experiencia de lectura y escritura con estilo Windows 11 mediante degradados, superficies tipo mica, rectángulos redondeados y fuentes integradas. El tema incluye cuatro variantes construidas con CSS modular.

## Características

- Estilo Fluent Design con degradados, mica, rectángulos redondeados e indicadores coloridos
- Cuatro variantes: Light, Dark, Ink e Ink Dark
- Estilos personalizados de CodeMirror para bloques de código
- Fuentes serif, manuscritas y monoespaciadas integradas

## Compatibilidad

- Windows 10 y Windows 11
- Aplicación de escritorio de Typora
- Cobertura de idiomas: inglés y chino (Source Han Serif CN). Los modos Ink también usan Ink Free y FZSJ-SGLDXMHJW como letra manuscrita.

## Capturas de pantalla

Liquid Theme busca ofrecer una experiencia visual moderna de Windows 11 en Typora. Usa elementos de interfaz como degradados, material tipo mica y rectángulos redondeados. El tema admite inglés y chino, y proporciona Light Mode, Dark Mode, Ink Mode e Ink Dark Mode.

![preview](/media/theme/liquid/preview.png)

### Light Mode

![light-preview1](/media/theme/liquid/light-preview1.png)

![light-preview2](/media/theme/liquid/light-preview2.png)

![light-preview3](/media/theme/liquid/light-preview3.png)

### Dark Mode

![dark-preview1](/media/theme/liquid/dark-preview1.png)

![dark-preview2](/media/theme/liquid/dark-preview2.png)

![dark-preview3](/media/theme/liquid/dark-preview3.png)

### Ink Mode & Ink Dark Mode

Si usas un PC 2 en 1 como Microsoft Surface para estudiar o escribir, o simplemente prefieres fuentes manuscritas, Ink Mode ofrece una experiencia de lectura y escritura con estilo manuscrito en Typora.

![ink-preview1](/media/theme/liquid/ink-preview1.png)

![ink-preview2](/media/theme/liquid/ink-preview2.png)

![ink-preview3](/media/theme/liquid/ink-preview3.png)

## Instalación

1. Descarga `liquid.zip` desde la página de [Releases](https://github.com/ruiyangzhou01/Liquid/releases).
2. En Typora, abre **Preferences** → **Appearance** → **Open Theme Folder**.
3. Descomprime y copia `liquid.css`, `liquid-dark.css`, `liquid-ink.css`, `liquid-ink-dark.css` y la carpeta de fuentes `liquid/` en la carpeta del tema.
4. Reinicia Typora.
5. Selecciona el tema Liquid en el menú **Themes**.
6. Abre `Demo.md` de este repositorio (o del archivo del código fuente) para previsualizar el resultado.

### Fuentes del modo Ink

Liquid incluye las fuentes Ink y las carga mediante `@font-face`, por lo que normalmente no es necesario instalarlas en el sistema. En sistemas sensibles a mayúsculas, asegúrate de que los nombres de archivo en `liquid/` coincidan con lo que espera el CSS (`inkfree.ttf` y `FZSJ-SGLDXMHJW.ttf`); renombra los archivos o ajusta el CSS si es necesario. `FZSJ-SGLDXMHJW` renderiza caracteres chinos en los modos Ink y `Inkfree` aporta la letra manuscrita para texto latino.

## Compilar desde el código fuente

Los scripts de compilación usan rutas de Windows.

1. Instala Python 3.
2. Ejecuta `cd src/Deploy`.
3. Ejecuta `python CombineCSS.py` para combinar `src/liquid*.css` en `dist/*.css`.
4. (Opcional) Ejecuta `cd ../deploy` y `python CompressZip.py` para empaquetar `dist` como `liquid.zip`.

## Personalización

- Añade CSS personalizado en Typora (recomendado): <https://support.typora.io/Add-Custom-CSS/>.
- Edita los archivos compilados en la carpeta del tema (`dist/*.css` en este repositorio).
- Para cambios más profundos, edita los módulos en `src/liquid/` y vuelve a compilar. Consulta la documentación abajo.

## Documentación

- [Documentación del tema Liquid](doc/Document_es.md)

## Licencia

[GPL-3.0 License](https://github.com/ruiyangzhou01/Liquid/blob/main/LICENSE) © ruiyangzhou01
