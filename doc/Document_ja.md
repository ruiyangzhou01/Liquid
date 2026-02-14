# Liquid テーマドキュメント

[English](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document.md) • [中文](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_zh.md) • [Deutsch](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_de.md) • [Español](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_es.md) • [Français](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_fr.md) • [日本語](https://github.com/ruiyangzhou01/Liquid/blob/main/doc/Document_ja.md)

## 概要
Liquid は Fluent スタイルの Typora テーマです。現在のリポジトリは `src/` を中心とした source-first 構成です。

## 構成
- エントリー: `src/liquid.css`, `src/liquid-dark.css`, `src/liquid-ink.css`, `src/liquid-ink-dark.css`
- モジュールとフォント: `src/liquid/`
- デモ: `Demo.md`
- ドキュメント: `doc/Document*.md`

## インストール
1. Typora のテーマフォルダを開く。
2. `src/liquid*.css` を 4 つコピー。
3. `src/liquid/` フォルダを CSS と同じ場所にコピー。
4. Typora を再起動してテーマを選択。

## モジュール
- レイアウト: `main.css`
- 色: `color-light.css`, `color-dark.css`
- フォント: `font.css`, `font-ink.css`
- コード: `CodeMirror.css`, `CodeMirror-dark.css`
- 調整: `custom-ink.css`, `custom-dark.css`

## 注意点
- Ink モードは `Inkfree` と `FZSJ-SGLDXMHJW` を使用。
- 大文字小文字を区別する環境ではファイル名を厳密に一致させてください。

## トラブルシューティング
- テーマが出ない: 4 つの CSS がテーマフォルダにあるか確認。
- フォントが効かない: `liquid/` が CSS の隣にあるか確認。
- 見た目が変わらない: カスタム CSS を一時的に無効化。
