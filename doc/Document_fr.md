# Documentation du thème Liquid

[English](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document.md) • [中文](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_zh.md) • [Deutsch](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_de.md) • [Español](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_es.md) • [Français](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_fr.md)

## Structure des fichiers

### Package de publication

```bash
│  liquid-dark.css
│  liquid-ink-dark.css
│  liquid-ink.css
│  liquid.css
│  Demo.md
│  Document.md
│
└─liquid # fichiers de polices utilisés par le thème
```

### Code source

```bash
├─.github
│  └─workflows
├─dist # fichiers CSS combinés
├─font # tous les fichiers de polices
├─media # images d'aperçu du thème Liquid
└─src # code source
   ├─Deploy # scripts Python pour créer les packages de publication
   └─liquid # composants CSS
```

## Utilisation

### Ajouter un CSS personnalisé (recommandé)

C'est la manière la plus simple de personnaliser le thème.

Voir <https://support.typora.io/Add-Custom-CSS/> pour plus d'informations.

### Modifier le fichier CSS publié

Installez le thème Liquid sur votre PC, puis modifiez le fichier `xxxxx.css` dans le dossier du thème.

### Modifier le code source du projet

Téléchargez `Source code (zip)` depuis la page [Releases](https://github.com/ruiyangzhou01/Liquid/releases) du [dépôt Liquid](https://github.com/ruiyangzhou01/Liquid/), puis modifiez les fichiers CSS dans le dossier `src`.
