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

Liquid は [Microsoft Fluent Design](https://www.microsoft.com/design/fluent/#/) と [Purple Theme](https://github.com/hliu202/typora-purple-theme) に着想を得た Typora テーマです。現在のリポジトリでは、`src/` に実運用可能なテーマファイルを直接配置しています（`dist/` の別ビルド成果物はありません）。

## 現在の状態

- 継続メンテナンス中、4 バリアントを提供：`liquid` / `liquid-dark` / `liquid-ink` / `liquid-ink-dark`
- ソース CSS とフォントをリポジトリに同梱
- ドキュメントと翻訳を現行構成に合わせて更新

## 特徴

- Fluent スタイル（グラデーション、角丸、アクセント表示）
- Light / Dark / Ink / Ink Dark の 4 モード
- CodeMirror のカスタムスタイル
- セリフ体・等幅・Ink 手書き向けフォントを同梱

## リポジトリ構成

```text
src/
  liquid.css
  liquid-dark.css
  liquid-ink.css
  liquid-ink-dark.css
  liquid/
    *.css
    *.ttf
    *.woff2
Demo.md
README*.md
doc/Document*.md
media/
assets/
```

## インストール

1. [Releases](https://github.com/ruiyangzhou01/Liquid/releases) から `liquid.zip` を取得するか、リポジトリを clone します。
2. Typora の **Preferences** → **Appearance** → **Open Theme Folder** を開きます。
3. 以下をテーマフォルダにコピーします：
   - `src/liquid.css`
   - `src/liquid-dark.css`
   - `src/liquid-ink.css`
   - `src/liquid-ink-dark.css`
   - `src/liquid/`（フォルダごと）
4. Typora を再起動し、Liquid テーマを選択します。
5. `Demo.md` を開いて表示を確認します。

## カスタマイズ

- 手早い調整：テーマフォルダ内の `liquid*.css` を直接編集。
- 詳細調整：`src/liquid/` のモジュール（`main.css`、`color-*.css`、`font*.css`、`CodeMirror*.css`、`custom-*.css`）を編集。
- Typora カスタム CSS で上書き追加：<https://support.typora.io/Add-Custom-CSS/>。

## トラブルシューティング

- **テーマが表示されない**：4 つの `liquid*.css` がテーマフォルダ直下にあるか確認。
- **Ink フォントが反映されない**：`liquid/` フォルダが CSS と同じ場所にあるか確認。
- **大文字小文字区別環境で文字欠け**：CSS 参照名（`Inkfree.ttf`、`FZSJ-SGLDXMHJW.TTF`）とファイル名を一致させてください。

## ドキュメント

- [Liquid テーマドキュメント](doc/Document_ja.md)

## ライセンス

[GPL-3.0 License](https://github.com/ruiyangzhou01/Liquid/blob/main/LICENSE) © ruiyangzhou01
