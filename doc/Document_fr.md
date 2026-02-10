# Documentation du thème Liquid

[English](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document.md) • [中文](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_zh.md) • [Deutsch](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_de.md) • [Español](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_es.md) • [Français](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_fr.md) • [日本語](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_ja.md)

## Vue d’ensemble

Liquid est un thème Typora inspiré de Microsoft Fluent Design. Ce document décrit l’organisation des fichiers, le workflow de build et les options de personnalisation selon le dépôt actuel.

## Structure des fichiers

### Paquet de release (`liquid.zip`)

L’archive de release est générée à partir du dossier `dist` et contient le CSS compilé et les polices :

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

### Organisation du dépôt

```text
Demo.md
README.md
README_*.md
LICENSE
media/                # images d’aperçu
font/                 # sources des polices
  JetBrainsMono-2.242/
  SourceHanSerifCN/
dist/                 # CSS compilé + ressources (contenu du release)
  liquid.css
  liquid-dark.css
  liquid-ink.css
  liquid-ink-dark.css
  liquid/
    *.ttf
    *.woff2
doc/                  # documentation traduite
src/
  liquid.css           # entrée (light)
  liquid-dark.css      # entrée (dark)
  liquid-ink.css       # entrée (ink)
  liquid-ink-dark.css  # entrée (ink dark)
  liquid/              # modules CSS
    main.css
    color-light.css
    color-dark.css
    font.css
    font-ink.css
    CodeMirror.css
    CodeMirror-dark.css
    custom-ink.css
    custom-dark.css
  Deploy/CombineCSS.py # combine @import vers dist
  deploy/CompressZip.py # empaquette dist en liquid.zip
```

## Construire depuis la source

Les scripts de build utilisent des chemins Windows et sont prévus pour Windows. CombineCSS.py se trouve dans `src/Deploy` (D majuscule) et CompressZip.py dans `src/deploy` (d minuscule). Sur les systèmes sensibles à la casse, utilisez le nom exact.

1. Installez Python 3.
2. Exécutez `cd src/Deploy`.
3. Exécutez `python CombineCSS.py` pour étendre `@import` de manière récursive et écrire dans `dist/`.
4. (Optionnel) Exécutez `cd ../deploy` et `python CompressZip.py` pour créer `liquid.zip` à partir de `dist`.

## Carte des modules CSS

Les fichiers d’entrée dans `src/` importent les modules de `src/liquid/` :

- `liquid.css` : mode light (importe `font.css`, `color-light.css`, `CodeMirror.css`, `main.css`).
- `liquid-dark.css` : mode dark (importe `font.css`, `color-dark.css`, `CodeMirror-dark.css`, `main.css`, `custom-dark.css`).
- `liquid-ink.css` : mode ink (importe `font-ink.css`, `color-light.css`, `CodeMirror.css`, `main.css`, `custom-ink.css`).
- `liquid-ink-dark.css` : mode ink dark (importe `font-ink.css`, `color-dark.css`, `CodeMirror-dark.css`, `main.css`, `custom-ink.css`, `custom-dark.css`).

Modules clés :

- `main.css` : mise en page partagée, typographie et composants.
- `color-light.css` / `color-dark.css` : variables de couleur pour palettes claires/sombres.
- `font.css` : polices par défaut (Source Han Serif CN + JetBrains Mono).
- `font-ink.css` : polices manuscrites (Ink Free + FZSJ-SGLDXMHJW).
- `CodeMirror.css` / `CodeMirror-dark.css` : styles des blocs de code.
- `custom-ink.css` : ajustements typographiques du mode Ink.
- `custom-dark.css` : ajustements UI du mode sombre.

## Options de personnalisation

### 1. Ajouter du CSS personnalisé (recommandé)

Utilisez le CSS personnalisé de Typora pour ajouter vos propres overrides. Voir <https://support.typora.io/Add-Custom-CSS/>.

### 2. Modifier les fichiers compilés

Après installation, modifiez directement `liquid.css`, `liquid-dark.css`, `liquid-ink.css` ou `liquid-ink-dark.css` dans le dossier du thème. Gardez le dossier `liquid/` à côté des fichiers CSS afin que `@font-face` fonctionne.

### 3. Modifier les modules source

Pour des changements plus profonds, modifiez les modules sous `src/liquid/` et reconstruisez avec `CombineCSS.py`. Modifications typiques :

- Couleurs : `color-light.css` et `color-dark.css`
- Polices : `font.css` et `font-ink.css`
- Blocs de code : `CodeMirror.css` et `CodeMirror-dark.css`
- Ajustements Ink/Dark : `custom-ink.css` et `custom-dark.css`
- Mise en page et typographie : `main.css`

## Notes sur les polices

Les modes Ink utilisent `Inkfree` pour l’écriture manuscrite latine et `FZSJ-SGLDXMHJW` pour les caractères chinois. Les polices sont incluses et chargées via `@font-face`, donc l’installation système n’est généralement pas nécessaire. Sur les systèmes sensibles à la casse, assurez-vous que les noms de fichiers dans `liquid/` correspondent au CSS (`inkfree.ttf` et `FZSJ-SGLDXMHJW.ttf`), ou renommez les fichiers/modifiez le CSS.
