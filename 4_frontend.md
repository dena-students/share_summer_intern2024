## ディレクトリ構成

```
├── api                      aspidaのAPI型定義ファイル
├── assets                   画像などのアセット
├── components
│   ├── functional           ロジックのみで完結するコンポーネント
│   ├── layout               レイアウトコンポーネント
│   ├── model                modelに関心をもつコンポーネント
│   ├── page                 ページに対応するコンポーネント
│   └── ui                   汎用コンポーネント
├── hooks                    カスタムフックス
├── libs                     外部パッケージ依存の設定ファイルなど
├── models                   アプリケーション用のドメインモデル
├── pages                    Next.jsが管理している各ページのroute
├── repositories             API接続のロジック
├── states                   グローバルステート管理
├── styles                   グローバルで適用するcss
└── utils                    汎用関数群
```

## 依存関係

View -> Hooks -> Repository
