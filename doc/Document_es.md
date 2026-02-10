# Documentación del tema Liquid

[English](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document.md) • [中文](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_zh.md) • [Deutsch](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_de.md) • [Español](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_es.md) • [Français](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_fr.md) • [日本語](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_ja.md)

## Descripción general

Liquid es un tema de Typora inspirado en Microsoft Fluent Design. Este documento explica la estructura de archivos, el flujo de compilación y las opciones de personalización según el repositorio actual.

## Estructura de archivos

### Paquete de lanzamiento (`liquid.zip`)

El archivo de lanzamiento se genera a partir de la carpeta `dist` y contiene el CSS compilado y las fuentes:

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

### Estructura del repositorio

```text
Demo.md
README.md
README_*.md
LICENSE
media/                # imágenes de vista previa
font/                 # fuentes originales
  JetBrainsMono-2.242/
  SourceHanSerifCN/
dist/                 # CSS compilado + recursos de fuentes (contenido del release)
  liquid.css
  liquid-dark.css
  liquid-ink.css
  liquid-ink-dark.css
  liquid/
    *.ttf
    *.woff2
doc/                  # documentación traducida
src/
  liquid.css           # entrada (light)
  liquid-dark.css      # entrada (dark)
  liquid-ink.css       # entrada (ink)
  liquid-ink-dark.css  # entrada (ink dark)
  liquid/              # módulos CSS
    main.css
    color-light.css
    color-dark.css
    font.css
    font-ink.css
    CodeMirror.css
    CodeMirror-dark.css
    custom-ink.css
    custom-dark.css
  Deploy/CombineCSS.py # combina @import en dist
  deploy/CompressZip.py # empaqueta dist como liquid.zip
```

## Compilar desde el código fuente

Los scripts de compilación usan rutas de Windows y están pensados para Windows. CombineCSS.py está en `src/Deploy` (D mayúscula) y CompressZip.py en `src/deploy` (d minúscula). En sistemas sensibles a mayúsculas utiliza el nombre exacto.

1. Instala Python 3.
2. Ejecuta `cd src/Deploy`.
3. Ejecuta `python CombineCSS.py` para expandir recursivamente `@import` y escribir en `dist/`.
4. (Opcional) Ejecuta `cd ../deploy` y `python CompressZip.py` para crear `liquid.zip` desde `dist`.

## Mapa de módulos CSS

Los archivos de entrada en `src/` importan módulos en `src/liquid/`:

- `liquid.css`: modo light (importa `font.css`, `color-light.css`, `CodeMirror.css`, `main.css`).
- `liquid-dark.css`: modo dark (importa `font.css`, `color-dark.css`, `CodeMirror-dark.css`, `main.css`, `custom-dark.css`).
- `liquid-ink.css`: modo ink (importa `font-ink.css`, `color-light.css`, `CodeMirror.css`, `main.css`, `custom-ink.css`).
- `liquid-ink-dark.css`: modo ink dark (importa `font-ink.css`, `color-dark.css`, `CodeMirror-dark.css`, `main.css`, `custom-ink.css`, `custom-dark.css`).

Módulos clave:

- `main.css`: diseño compartido, tipografía y componentes.
- `color-light.css` / `color-dark.css`: variables de color para paletas claras y oscuras.
- `font.css`: fuentes predeterminadas (Source Han Serif CN + JetBrains Mono).
- `font-ink.css`: fuentes manuscritas (Ink Free + FZSJ-SGLDXMHJW).
- `CodeMirror.css` / `CodeMirror-dark.css`: estilos para bloques de código.
- `custom-ink.css`: ajustes tipográficos del modo Ink.
- `custom-dark.css`: ajustes de UI del modo oscuro.

## Opciones de personalización

### 1. Añadir CSS personalizado (recomendado)

Usa el CSS personalizado de Typora para añadir tus propias modificaciones. Consulta <https://support.typora.io/Add-Custom-CSS/>.

### 2. Editar los archivos compilados

Tras instalar el tema, edita directamente `liquid.css`, `liquid-dark.css`, `liquid-ink.css` o `liquid-ink-dark.css` en la carpeta del tema. Mantén la carpeta `liquid/` junto a los CSS para que las declaraciones `@font-face` se resuelvan correctamente.

### 3. Editar los módulos fuente

Para cambios profundos, edita los módulos en `src/liquid/` y recompila con `CombineCSS.py`. Ajustes típicos:

- Colores: `color-light.css` y `color-dark.css`
- Fuentes: `font.css` y `font-ink.css`
- Bloques de código: `CodeMirror.css` y `CodeMirror-dark.css`
- Ajustes Ink/Dark: `custom-ink.css` y `custom-dark.css`
- Diseño y tipografía: `main.css`

## Notas sobre fuentes

Los modos Ink usan `Inkfree` para manuscrito latino y `FZSJ-SGLDXMHJW` para caracteres chinos. Las fuentes se incluyen y se cargan mediante `@font-face`, por lo que normalmente no hace falta instalarlas en el sistema. En sistemas sensibles a mayúsculas, asegúrate de que los nombres de archivo en `liquid/` coincidan con el CSS (`inkfree.ttf` y `FZSJ-SGLDXMHJW.ttf`), o renombra los archivos/ajusta el CSS.
