# Liquid Theme Documentation

[English](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document.md) • [中文](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_zh.md) • [Deutsch](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_de.md) • [Español](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_es.md) • [Français](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_fr.md)

## File Structure

### Release Package

```bash
│  liquid-dark.css
│  liquid-ink-dark.css
│  liquid-ink.css
│  liquid.css
│  Demo.md
│  Document.md
│
└─liquid # font files used by the theme
```

### Source Code

```bash
├─.github
│  └─workflows
├─dist # combined CSS files
├─font # all font files
├─media # preview images for Liquid Theme
└─src # source code
   ├─Deploy # Python scripts to build release packages
   └─liquid # CSS partials
```

## Usage

### Add Custom CSS (Recommended)

This is the easiest way to customize the theme.

See <https://support.typora.io/Add-Custom-CSS/> for guidance.

### Modify the Released CSS File

Install the Liquid Theme on your PC, then modify the `xxxxx.css` file in the theme folder.

### Modify Source Code of Project

Download the `Source code (zip)` from the [Releases](https://github.com/ruiyangzhou01/Liquid/releases) page of the [Liquid repository](https://github.com/ruiyangzhou01/Liquid/), then modify the CSS files under the `src` folder.
