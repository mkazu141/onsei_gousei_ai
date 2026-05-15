---
version: "1.0"
name: 対話Agent管理画面
description: >
  対話型Agentを管理・監視するWebアプリケーション（React + Vite + Tailwind CSS v4）のデザインシステム。
  ブランドカラーは青系（#0157E9）を軸に、情報密度の高い管理UIを構築する。
  アイコンはLucide React、スタイリングはTailwind CSS v4 の @theme ブロックでトークンを一元管理する。

colors:
  primary: "#0157E9"
  primary-dark: "#002B60"
  secondary: "#336699"
  secondary-light: "#337AB7"
  warning: "#F0C600"
  selected: "#DBEAFE"
  success: "#29A85D"
  surface-white: "#FFFFFF"
  surface-gray: "#F0F3F7"
  header-bg: "#0F1B33"
  border: "#D7DADD"

typography:
  display-sm:
    fontFamily: '"メイリオ", Meiryo, "Hiragino Kaku Gothic ProN", sans-serif'
    fontSize: 20px
    fontWeight: 700
    lineHeight: 1.3
  title-lg:
    fontFamily: '"メイリオ", Meiryo, "Hiragino Kaku Gothic ProN", sans-serif'
    fontSize: 18px
    fontWeight: 700
    lineHeight: 1.35
  title-md:
    fontFamily: '"メイリオ", Meiryo, "Hiragino Kaku Gothic ProN", sans-serif'
    fontSize: 16px
    fontWeight: 600
    lineHeight: 1.4
  title-sm:
    fontFamily: '"メイリオ", Meiryo, "Hiragino Kaku Gothic ProN", sans-serif'
    fontSize: 14px
    fontWeight: 600
    lineHeight: 1.4
  body-md:
    fontFamily: '"メイリオ", Meiryo, "Hiragino Kaku Gothic ProN", sans-serif'
    fontSize: 13px
    fontWeight: 400
    lineHeight: 1.6
  body-sm:
    fontFamily: '"メイリオ", Meiryo, "Hiragino Kaku Gothic ProN", sans-serif'
    fontSize: 12px
    fontWeight: 400
    lineHeight: 1.5
  caption:
    fontFamily: '"メイリオ", Meiryo, "Hiragino Kaku Gothic ProN", sans-serif'
    fontSize: 11px
    fontWeight: 500
    lineHeight: 1.4
    letterSpacing: 0.3px
  button:
    fontFamily: '"メイリオ", Meiryo, "Hiragino Kaku Gothic ProN", sans-serif'
    fontSize: 13px
    fontWeight: 700
    lineHeight: 1.0
  nav-link:
    fontFamily: '"メイリオ", Meiryo, "Hiragino Kaku Gothic ProN", sans-serif'
    fontSize: 13px
    fontWeight: 400
    lineHeight: 1.4

rounded:
  sm: 4px
  md: 6px
  lg: 8px
  xl: 12px
  pill: 9999px

spacing:
  xxs: 4px
  xs: 8px
  sm: 12px
  md: 16px
  lg: 24px
  xl: 32px
  xxl: 48px
  header-h: 60px
  sidebar-w: 240px
---

# DESIGN.md

## 概要

本ドキュメントは、対話Agentのモック開発における**ビジュアルデザインの基本仕様**を定義します。

### 技術基盤

| 項目 | 採用技術 |
|------|----------|
| **フレームワーク** | React (Vite) |
| **スタイリング** | Tailwind CSS v4 |
| **アイコン** | Lucide React |

### Tailwind CSS 設定

本デザインシステムの値は **Tailwind CSS v4 の `@theme` ブロック**（通常は `src/index.css`）に集約して定義します。コンポーネント側ではハードコードされた値を直接記述せず、必ず `@theme` 由来のトークンを利用してください。

---

## カラーパレット

### メインカラー (Primary)

ブランドカラーは**青系**です。

| トークン | カラーコード | 用途 |
|----------|-------------|------|
| `primary` | `#0157E9` | プライマリボタン、リンク、アクティブ状態 |
| `primary-dark` | `#002B60` | ホバー・プレス状態、強調表示 |

### サブカラー (Secondary)

| トークン | カラーコード | 用途 |
|----------|-------------|------|
| `secondary` | `#336699` | セカンダリボタン、見出し背景 |
| `secondary-light` | `#337AB7` | 補助的なUI要素、サブアクション |

### アクセントカラー (Accent / Semantic)

| トークン | カラーコード | 用途 |
|----------|-------------|------|
| `warning` | `#F0C600` | 警告メッセージ、注意バッジ |
| `selected` | `#DBEAFE` | 選択アイテムのハイライト（青系ベースに馴染む薄青） |
| `success` | `#29A85D` | 成功メッセージ、完了・正常状態バッジ |

### サーフェス & ボーダー (Surface)

| トークン | カラーコード | 用途 |
|----------|-------------|------|
| `surface-white` | `#FFFFFF` | メイン背景、カード背景 |
| `surface-gray` | `#F0F3F7` | セクション背景、パネル背景、テーブル行背景 |
| `header-bg` | `#0F1B33` | グローバルヘッダー背景 |
| `border` | `#D7DADD` | 境界線、区切り線、入力枠線 |

---

## タイポグラフィ

### フォントファミリー

```
font-family: "メイリオ", Meiryo, "Hiragino Kaku Gothic ProN", sans-serif;
```

### スケール

| トークン | サイズ | ウェイト | 行間 | 用途 |
|----------|--------|----------|------|------|
| `display-sm` | 20px | 700 | 1.3 | メインページタイトル |
| `title-lg` | 18px | 700 | 1.35 | モーダルタイトル、セクション大見出し |
| `title-md` | 16px | 600 | 1.4 | カード見出し、サブセクション |
| `title-sm` | 14px | 600 | 1.4 | テーブルヘッダー、ラベル |
| `body-md` | 13px | 400 | 1.6 | 標準テキスト、説明文、テーブルセル |
| `body-sm` | 12px | 400 | 1.5 | 補助テキスト、メタ情報 |
| `caption` | 11px | 500 | 1.4 | バッジラベル、タグ、タイムスタンプ |
| `button` | 13px | 700 | 1.0 | ボタンラベル |
| `nav-link` | 13px | 400 | 1.4 | ナビゲーション項目 |

---

## スペーシング

基本単位は **4px** です。

### スペーシングスケール

| トークン | 値 | 用途 |
|----------|-----|------|
| `xxs` | 4px | 最小余白（アイコン隣接など） |
| `xs` | 8px | インライン要素間 |
| `sm` | 12px | フォーム要素内補助余白 |
| `md` | 16px | コンテナパディング、標準マージン |
| `lg` | 24px | カード内パディング、セクション区切り |
| `xl` | 32px | ページセクション内余白 |
| `xxl` | 48px | セクション間の大きな余白 |

### 要素サイズ

| トークン | 値 | 説明 |
|----------|-----|------|
| `header-h` | 60px | グローバルヘッダー高さ |
| `sidebar-w` | 240px | サイドバーナビゲーション幅 |

### パディング早見表

| 要素 | パディング |
|------|-----------|
| ボタン | `8px 16px` |
| テキスト入力 / セレクトボックス | `8px 12px` |
| カード | `20px` |
| モーダル | `24px` |

### 要素高さ

| 要素 | 高さ |
|------|------|
| ボタン（標準） | `36px` |
| テキスト入力 / セレクトボックス | `36px` |

---

## ボーダーラジアス

| トークン | 値 | 用途 |
|----------|-----|------|
| `rounded.sm` | 4px | バッジ、タグ |
| `rounded.md` | 6px | ボタン、テキスト入力 |
| `rounded.lg` | 8px | カード、パネル |
| `rounded.xl` | 12px | モーダル |
| `rounded.pill` | 9999px | ステータスバッジ、アバター |

---

## アイコン

### アイコンシステム

**Lucide React** を使用します。サイズは Tailwind の `h-*` / `w-*` クラスで制御します。

### サイズ

| サイズ | 値 | Tailwind クラス | 用途 |
|--------|-----|----------------|------|
| 小 | 16×16px | `h-4 w-4` | インラインアイコン、テキスト内 |
| 中 | 20×20px | `h-5 w-5` | ボタン内、入力フィールド内 |
| 標準 | 24×24px | `h-6 w-6` | ナビゲーション、標準UI要素 |
| 大 | 32×32px | `h-8 w-8` | ヘッダー、主要アクションエリア |

### カラー

| 状態 | カラーコード | Tailwind クラス例 |
|------|-------------|-------------------|
| デフォルト | `#646464` | `text-gray-500` |
| アクティブ | `#0157E9` | `text-primary` |
| ホバー | `#002B60` | `text-primary-dark` |
| 非アクティブ | `#D7DADD` | `text-border` |
