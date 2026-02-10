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

Liquid est un thème Typora inspiré par [Microsoft Fluent Design](https://www.microsoft.com/design/fluent/#/) et le [Purple Theme](https://github.com/hliu202/typora-purple-theme). Il offre une expérience de lecture et d’écriture de style Windows 11 grâce aux dégradés, aux surfaces de type mica, aux rectangles arrondis et aux polices intégrées. Le thème propose quatre variantes basées sur du CSS modulaire.

## Fonctionnalités

- Style Fluent Design avec dégradés, mica, rectangles arrondis et indicateurs colorés
- Quatre variantes : Light, Dark, Ink et Ink Dark
- Styles CodeMirror personnalisés pour les blocs de code
- Polices serif, manuscrites et monospace intégrées

## Compatibilité

- Windows 10 et Windows 11
- Application de bureau Typora
- Couverture linguistique : anglais et chinois (Source Han Serif CN). Les modes Ink utilisent également Ink Free et FZSJ-SGLDXMHJW pour l’écriture manuscrite.

## Captures d’écran

Liquid Theme vise à offrir une expérience visuelle moderne de Windows 11 dans Typora. Il utilise des éléments d’interface comme les dégradés, la matière mica et les rectangles arrondis. Le thème prend en charge l’anglais et le chinois et propose Light Mode, Dark Mode, Ink Mode et Ink Dark Mode.

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

Si vous utilisez un PC 2-en-1 comme Microsoft Surface pour étudier ou écrire, ou si vous préférez simplement les polices manuscrites, Ink Mode offre une expérience de lecture et d’écriture manuscrite dans Typora.

![ink-preview1](/media/theme/liquid/ink-preview1.png)

![ink-preview2](/media/theme/liquid/ink-preview2.png)

![ink-preview3](/media/theme/liquid/ink-preview3.png)

## Installation

1. Téléchargez `liquid.zip` depuis la page [Releases](https://github.com/ruiyangzhou01/Liquid/releases).
2. Dans Typora, ouvrez **Preferences** → **Appearance** → **Open Theme Folder**.
3. Décompressez et copiez `liquid.css`, `liquid-dark.css`, `liquid-ink.css`, `liquid-ink-dark.css` ainsi que le dossier de polices `liquid/` dans le dossier du thème.
4. Redémarrez Typora.
5. Sélectionnez le thème Liquid dans le menu **Themes**.
6. Ouvrez `Demo.md` depuis ce dépôt (ou l’archive du code source) pour prévisualiser le rendu.

### Polices du mode Ink

Installez `FZSJ-SGLDXMHJW.TTF` depuis `dist/liquid` (ou le dossier `liquid/` du release) pour afficher les caractères chinois en mode Ink. `Inkfree.ttf` fournit la police manuscrite pour le texte latin.

## Construire depuis la source

Les scripts de build utilisent des chemins Windows.

1. Installez Python 3.
2. Exécutez `cd src/Deploy`.
3. Exécutez `python CombineCSS.py` pour combiner `src/liquid*.css` dans `dist/*.css`.
4. (Optionnel) Exécutez `cd ../deploy` et `python CompressZip.py` pour empaqueter `dist` en `liquid.zip`.

## Personnalisation

- Ajoutez du CSS personnalisé dans Typora (recommandé) : <https://support.typora.io/Add-Custom-CSS/>.
- Modifiez les fichiers compilés dans le dossier du thème (`dist/*.css` dans ce dépôt).
- Pour des changements plus profonds, modifiez les modules dans `src/liquid/` et reconstruisez. Consultez la documentation ci-dessous.

## Documentation

- [Documentation du thème Liquid](doc/Document_fr.md)

## Licence

[GPL-3.0 License](https://github.com/ruiyangzhou01/Liquid/blob/main/LICENSE) © ruiyangzhou01
