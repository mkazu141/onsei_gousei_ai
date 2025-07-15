# プロジェクト設計概要

## 目的

* 管理画面とチャット画面に分かれた構成でチャットボットサービスを構築する
* 管理画面ではQA生成とプロンプト編集が可能
* チャット画面ではユーザーが生成AIチャットボットを利用できる

---

## 画面構成

### 1. 管理画面 (Admin UI)

* URL: `/admin/*`
* 機能:

  * ログイン画面 (後日実装)
  * QA生成画面

    * PDFファイルアップロード
    * QA生成トリガー
    * QA (CSV) ダウンロード
  * プロンプト編集画面

    * プロンプト一覧取得
    * プロンプト編集
    * 保存 (バックエンドAPI経由)

### 2. チャット画面 (User UI)

* URL: `/chat/*`
* 機能:

  * ログイン画面 (後日実装)
  * チャットボット画面 (後日実装)

---

## 技術スタック

### フロントエンド

* React + Vite
* Zustand or React Context (状態管理)
* Axios (API通信)
* Tailwind CSS + shadcn/ui

### バックエンド

* FastAPI (Python)
* SQLAlchemy
* JWT認証 (Admin/User)
* LangChain (必要時)

### その他

* Docker Compose

---

## API設計概要

### 管理画面用

| エンドポイント                   | Method | 機能           |
| ------------------------- | ------ | ------------ |
| `/api/admin/login`        | POST   | 管理者ログイン      |
| `/api/admin/prompts`      | GET    | プロンプト一覧取得    |
| `/api/admin/prompts/{id}` | PUT    | プロンプト更新      |
| `/api/admin/qa/upload`    | POST   | PDFアップロード    |
| `/api/admin/qa/download`  | GET    | QA CSVダウンロード |

### チャット画面用

| エンドポイント           | Method | 機能       |
| ----------------- | ------ | -------- |
| `/api/user/login` | POST   | ユーザーログイン |
| `/api/chat`       | POST   | チャット送信   |

---

## フロントエンドディレクトリ構成案

```
ui/
├── src/
│   ├── admin/
│   │   ├── pages/
│   │   ├── components/
│   ├── chat/
│   │   ├── pages/
│   │   ├── components/
│   ├── api/
│   ├── hooks/
│   ├── App.jsx
│   └── main.jsx
```

---

## ライセンス管理ポリシー

* GPL, AGPL ライセンス禁止
* MIT, BSD, Apache 2.0 のみ使用可
* 新規OSS導入時はライセンス確認必須
* npm list --depth=0、pip-licenses等で定期チェック

---

## Copilot用プロンプト例 (抜粋)

### QA生成画面

```jsx
// Reactコンポーネント：QA生成画面
// - PDFアップロード
// - API POST
// - CSVダウンロード
// - useState, axios 使用
```

### プロンプト編集画面

```jsx
// Reactコンポーネント：プロンプト編集画面
// - プロンプト一覧取得
// - 編集フォーム
// - 保存ボタン
// - useEffect, axios 使用
```

---

## 今後のタスク

* ログイン画面実装 (管理/ユーザー)
* チャット画面実装
* API認証スキーム詳細設計 (JWTスコープ分け)
