# Liquid Theme Dokumentation

[English](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document.md) • [中文](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_zh.md) • [Deutsch](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_de.md) • [Español](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_es.md) • [Français](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_fr.md)

## Dateistruktur

### Release-Paket

```bash
│  liquid-dark.css
│  liquid-ink-dark.css
│  liquid-ink.css
│  liquid.css
│  Demo.md
│  Document.md
│
└─liquid # vom Theme verwendete Schriftdateien
```

### Quellcode

```bash
├─.github
│  └─workflows
├─dist # kombinierte CSS-Dateien
├─font # alle Schriftdateien
├─media # Vorschaubilder für Liquid Theme
└─src # Quellcode
   ├─Deploy # Python-Skripte zum Erstellen von Release-Paketen
   └─liquid # CSS-Teile
```

## Verwendung

### Eigenes CSS hinzufügen (empfohlen)

Dies ist der einfachste Weg, das Theme anzupassen.

Siehe <https://support.typora.io/Add-Custom-CSS/> für Hinweise.

### Die veröffentlichte CSS-Datei ändern

Installieren Sie das Liquid Theme auf Ihrem PC und bearbeiten Sie dann die Datei `xxxxx.css` im Theme-Ordner.

### Den Quellcode des Projekts ändern

Laden Sie `Source code (zip)` von der [Releases](https://github.com/ruiyangzhou01/Liquid/releases)-Seite des [Liquid-Repositorys](https://github.com/ruiyangzhou01/Liquid/) herunter und bearbeiten Sie die CSS-Dateien im Ordner `src`.
