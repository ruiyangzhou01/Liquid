# Liquid-Theme-Dokumentation

[English](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document.md) • [中文](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_zh.md) • [Deutsch](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_de.md) • [Español](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_es.md) • [Français](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_fr.md) • [日本語](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_ja.md)

## Überblick

Liquid ist ein Typora-Theme, das von Microsoft Fluent Design inspiriert wurde. Dieses Dokument beschreibt die Dateistruktur, den Build-Workflow und die Anpassungsmöglichkeiten basierend auf dem aktuellen Repository.

## Dateistruktur

### Release-Paket (`liquid.zip`)

Das Release-Archiv wird aus dem Ordner `dist` erzeugt und enthält die kompilierten CSS-Dateien sowie die Schriftarten:

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

### Repository-Layout

```text
Demo.md
README.md
README_*.md
LICENSE
media/                # Vorschaubilder
font/                 # Originale Schriftquellen
  JetBrainsMono-2.242/
  SourceHanSerifCN/
dist/                 # Kompilierte CSS + Schrift-Assets (Release-Inhalt)
  liquid.css
  liquid-dark.css
  liquid-ink.css
  liquid-ink-dark.css
  liquid/
    *.ttf
    *.woff2
doc/                  # Übersetzte Dokumentation
src/
  liquid.css           # Einstieg (light)
  liquid-dark.css      # Einstieg (dark)
  liquid-ink.css       # Einstieg (ink)
  liquid-ink-dark.css  # Einstieg (ink dark)
  liquid/              # CSS-Module
    main.css
    color-light.css
    color-dark.css
    font.css
    font-ink.css
    CodeMirror.css
    CodeMirror-dark.css
    custom-ink.css
    custom-dark.css
  Deploy/CombineCSS.py # kombiniert @import in dist
  deploy/CompressZip.py # packt dist als liquid.zip
```

## Build aus dem Quellcode

Die Build-Skripte verwenden Windows-Pfade und sind für Windows gedacht.

1. Python 3 installieren.
2. `cd src/Deploy` ausführen.
3. `python CombineCSS.py` ausführen, um `@import` rekursiv zu erweitern und nach `dist/` zu schreiben.
4. (Optional) `cd ../deploy` und `python CompressZip.py` ausführen, um `liquid.zip` aus `dist` zu erzeugen.

## CSS-Modulübersicht

Die Einstiegspunkte unter `src/` importieren Module aus `src/liquid/`:

- `liquid.css`: Light-Modus (importiert `font.css`, `color-light.css`, `CodeMirror.css`, `main.css`).
- `liquid-dark.css`: Dark-Modus (importiert `font.css`, `color-dark.css`, `CodeMirror-dark.css`, `main.css`, `custom-dark.css`).
- `liquid-ink.css`: Ink-Modus (importiert `font-ink.css`, `color-light.css`, `CodeMirror.css`, `main.css`, `custom-ink.css`).
- `liquid-ink-dark.css`: Ink-Dark-Modus (importiert `font-ink.css`, `color-dark.css`, `CodeMirror-dark.css`, `main.css`, `custom-ink.css`, `custom-dark.css`).

Wichtige Module:

- `main.css`: Gemeinsames Layout, Typografie und Komponenten.
- `color-light.css` / `color-dark.css`: Farbvariablen für helle/dunkle Paletten.
- `font.css`: Standardschriften (Source Han Serif CN + JetBrains Mono).
- `font-ink.css`: Handschrift-Schriften (Ink Free + FZSJ-SGLDXMHJW).
- `CodeMirror.css` / `CodeMirror-dark.css`: Styles für Codeblöcke.
- `custom-ink.css`: Ink-spezifische Typografie-Anpassungen.
- `custom-dark.css`: UI-Anpassungen für den Dark-Modus.

## Anpassungsoptionen

### 1. Eigenes CSS hinzufügen (empfohlen)

Nutze Typoras benutzerdefiniertes CSS, um eigene Overrides hinzuzufügen. Siehe <https://support.typora.io/Add-Custom-CSS/>.

### 2. Kompilierte Theme-Dateien bearbeiten

Nach der Installation können `liquid.css`, `liquid-dark.css`, `liquid-ink.css` oder `liquid-ink-dark.css` im Theme-Ordner direkt angepasst werden. Der Ordner `liquid/` mit den Schriftarten muss neben den CSS-Dateien bleiben, damit `@font-face` funktioniert.

### 3. Quellmodule bearbeiten

Für tiefere Anpassungen bearbeite die Module unter `src/liquid/` und baue mit `CombineCSS.py` neu. Typische Änderungen:

- Farben: `color-light.css` und `color-dark.css`
- Schriften: `font.css` und `font-ink.css`
- Codeblöcke: `CodeMirror.css` und `CodeMirror-dark.css`
- Ink/Dark-Anpassungen: `custom-ink.css` und `custom-dark.css`
- Layout und Typografie: `main.css`

## Hinweise zu Schriftarten

Die Ink-Modi nutzen `Inkfree.ttf` für lateinische Handschrift und `FZSJ-SGLDXMHJW.TTF` für chinesische Zeichen. Installiere `FZSJ-SGLDXMHJW.TTF` lokal, wenn du chinesische Zeichen im Ink-Modus benötigst.
