# Liquid-Theme-Dokumentation

[English](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document.md) • [中文](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_zh.md) • [Deutsch](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_de.md) • [Español](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_es.md) • [Français](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_fr.md) • [日本語](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_ja.md)

## Überblick
Liquid ist ein Typora-Theme im Fluent-Stil. Die aktuelle Struktur ist source-first: alles liegt unter `src/`.

## Struktur
- Einstieg: `src/liquid.css`, `src/liquid-dark.css`, `src/liquid-ink.css`, `src/liquid-ink-dark.css`
- Module und Fonts: `src/liquid/`
- Vorschau: `Demo.md`
- Doku: `doc/Document*.md`

## Installation
1. Typora-Theme-Ordner öffnen.
2. Vier `src/liquid*.css` kopieren.
3. Ordner `src/liquid/` daneben kopieren.
4. Typora neu starten und Theme wählen.

## Module
- Layout: `main.css`
- Farben: `color-light.css`, `color-dark.css`
- Schrift: `font.css`, `font-ink.css`
- Code: `CodeMirror.css`, `CodeMirror-dark.css`
- Overrides: `custom-ink.css`, `custom-dark.css`

## Hinweise
- Ink nutzt `Inkfree` und `FZSJ-SGLDXMHJW`.
- Auf dateisensitiven Systemen Dateinamen exakt beibehalten.

## Fehlerbehebung
- Theme fehlt: prüfen, ob alle vier CSS-Dateien im Theme-Ordner liegen.
- Schrift fehlt: prüfen, ob `liquid/` neben den CSS-Dateien liegt.
- Keine Änderung sichtbar: testweise Custom CSS deaktivieren.
