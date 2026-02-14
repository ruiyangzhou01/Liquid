# Documentation du thème Liquid

[English](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document.md) • [中文](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_zh.md) • [Deutsch](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_de.md) • [Español](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_es.md) • [Français](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_fr.md) • [日本語](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_ja.md)

## Vue d’ensemble
Liquid est un thème Typora de style Fluent. Le dépôt actuel utilise une structure source-first sous `src/`.

## Structure
- Entrées : `src/liquid.css`, `src/liquid-dark.css`, `src/liquid-ink.css`, `src/liquid-ink-dark.css`
- Modules et polices : `src/liquid/`
- Démo : `Demo.md`
- Documentation : `doc/Document*.md`

## Installation
1. Ouvrez le dossier de thèmes Typora.
2. Copiez les quatre `src/liquid*.css`.
3. Copiez le dossier complet `src/liquid/` à côté des CSS.
4. Redémarrez Typora et sélectionnez le thème.

## Modules
- Mise en page : `main.css`
- Couleurs : `color-light.css`, `color-dark.css`
- Polices : `font.css`, `font-ink.css`
- Code : `CodeMirror.css`, `CodeMirror-dark.css`
- Ajustements : `custom-ink.css`, `custom-dark.css`

## Notes
- Le mode Ink utilise `Inkfree` et `FZSJ-SGLDXMHJW`.
- Sur les systèmes sensibles à la casse, gardez exactement les noms de fichiers.

## Dépannage
- Thème absent : vérifiez la présence des quatre CSS dans le dossier de thèmes.
- Police absente : vérifiez que `liquid/` est copié à côté des CSS.
- Aucun changement visuel : désactivez temporairement le CSS personnalisé.
