# PDF Impose

A4縦PDFをA3横2アップに面付け変換するWebアプリ。

https://masaki-k-git.github.io/A4x2-to-A3/

**ブラウザ完結 — ファイルはサーバーに送信されません。**

## 使い方

1. PDFをドロップまたはクリックして選択
2. "Convert" ボタンをクリック
3. 変換完了後、ダウンロード

## 配置ルール

```
A3シート1: [page 1][page 2]
A3シート2: [page 3][page 4]
A3シート3: [page 5][page 6]
...
```

## 仕様

- 入力: A4縦 PDF
- 出力: A3横 PDF（2アップ）
- スケール: 70.7%（1/√2 等比）
- 奇数ページ: 末尾に空白ページを自動補完
- 依存: [pdf-lib](https://pdf-lib.js.org/) 1.17.1（CDN）

## ローカルで実行

```bash
# 任意のHTTPサーバーで index.html を開く
npx serve .
# または
python3 -m http.server 8080
```

## GitHub Pagesへのデプロイ

1. このリポジトリをフォーク or クローン
2. Settings → Pages → Source: `main` branch / `/ (root)`
3. `https://<username>.github.io/<repo-name>/` でアクセス可能

## ライセンス

MIT
