# Liquid テーマドキュメント

[English](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document.md) • [中文](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_zh.md) • [Deutsch](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_de.md) • [Español](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_es.md) • [Français](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_fr.md) • [日本語](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_ja.md)

## 概要

Liquid は Microsoft Fluent Design に着想を得た Typora テーマです。本ドキュメントでは、現在のリポジトリ構成に基づいたファイル配置、ビルド手順、カスタマイズ方法を説明します。

## ファイル構成

### リリースパッケージ（`liquid.zip`）

リリースアーカイブは `dist` フォルダから生成され、コンパイル済み CSS とフォントを含みます。

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

### リポジトリ構成

```text
Demo.md
README.md
README_*.md
LICENSE
media/                # プレビュー画像
font/                 # フォントの元データ
  JetBrainsMono-2.242/
  SourceHanSerifCN/
dist/                 # コンパイル済み CSS + フォント（リリース内容）
  liquid.css
  liquid-dark.css
  liquid-ink.css
  liquid-ink-dark.css
  liquid/
    *.ttf
    *.woff2
doc/                  # ドキュメント翻訳
src/
  liquid.css           # エントリ (light)
  liquid-dark.css      # エントリ (dark)
  liquid-ink.css       # エントリ (ink)
  liquid-ink-dark.css  # エントリ (ink dark)
  liquid/              # CSS モジュール
    main.css
    color-light.css
    color-dark.css
    font.css
    font-ink.css
    CodeMirror.css
    CodeMirror-dark.css
    custom-ink.css
    custom-dark.css
  Deploy/CombineCSS.py # @import を結合して dist に出力
  deploy/CompressZip.py # dist を liquid.zip にパッケージ
```

## ソースからビルド

ビルドスクリプトは Windows のパス表記を前提にしています。CombineCSS.py は `src/Deploy`（D 大文字）、CompressZip.py は `src/deploy`（d 小文字）にあります。大文字小文字を区別する環境では正確なフォルダ名を使用してください。

1. Python 3 をインストールします。
2. `cd src/Deploy` を実行します。
3. `python CombineCSS.py` を実行し、`@import` を再帰的に展開して `dist/` に出力します。
4. （任意）`cd ../deploy` と `python CompressZip.py` を実行し、`dist` から `liquid.zip` を作成します。

## CSS モジュール一覧

`src/` 配下のエントリ CSS は `src/liquid/` のモジュールを読み込みます。

- `liquid.css`：light モード（`font.css`、`color-light.css`、`CodeMirror.css`、`main.css`）。
- `liquid-dark.css`：dark モード（`font.css`、`color-dark.css`、`CodeMirror-dark.css`、`main.css`、`custom-dark.css`）。
- `liquid-ink.css`：ink モード（`font-ink.css`、`color-light.css`、`CodeMirror.css`、`main.css`、`custom-ink.css`）。
- `liquid-ink-dark.css`：ink dark モード（`font-ink.css`、`color-dark.css`、`CodeMirror-dark.css`、`main.css`、`custom-ink.css`、`custom-dark.css`）。

主要モジュール：

- `main.css`：共通レイアウト、タイポグラフィ、コンポーネント。
- `color-light.css` / `color-dark.css`：ライト/ダークの配色変数。
- `font.css`：標準フォント（Source Han Serif CN + JetBrains Mono）。
- `font-ink.css`：手書きフォント（Ink Free + FZSJ-SGLDXMHJW）。
- `CodeMirror.css` / `CodeMirror-dark.css`：コードブロックのスタイル。
- `custom-ink.css`：Ink モード向けのタイポグラフィ調整。
- `custom-dark.css`：Dark モード向けの UI 調整。

## カスタマイズ方法

### 1. カスタム CSS を追加（推奨）

Typora のカスタム CSS 機能を使って上書きします。詳しくは <https://support.typora.io/Add-Custom-CSS/> を参照してください。

### 2. コンパイル済みテーマを編集

テーマをインストールした後、テーマフォルダ内の `liquid.css`、`liquid-dark.css`、`liquid-ink.css`、`liquid-ink-dark.css` を直接編集できます。`@font-face` が解決できるように `liquid/` フォントフォルダを CSS の隣に置いてください。

### 3. ソースモジュールを編集

より深く調整する場合は `src/liquid/` のモジュールを編集し、`CombineCSS.py` で再ビルドします。よく触る箇所：

- 色：`color-light.css` と `color-dark.css`
- フォント：`font.css` と `font-ink.css`
- コードブロック：`CodeMirror.css` と `CodeMirror-dark.css`
- Ink/Dark 調整：`custom-ink.css` と `custom-dark.css`
- レイアウトとタイポグラフィ：`main.css`

## フォントに関する注意

Ink モードでは、ラテン文字に `Inkfree`、中国語に `FZSJ-SGLDXMHJW` を使用します。フォントは同梱され `@font-face` で読み込まれるため、通常はシステムへのインストールは不要です。大文字小文字を区別する環境では `liquid/` のファイル名が CSS の参照（`inkfree.ttf` と `FZSJ-SGLDXMHJW.ttf`）と一致するよう確認し、必要に応じてリネームまたは CSS を調整してください。
