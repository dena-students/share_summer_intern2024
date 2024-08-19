## ディレクトリ構成

```
.
├── cmd         バッチ処理などのエントリーポイント
├── config      環境変数などを管理
├── controller  HTTPリクエスト・レスポンスが責務。ロジックは持たない。openapiが持つサーバーのインターフェースを満たす。openapiに依存するのはこのパッケージのみ。
├── entity      ドメインのエンティティモデルやロジック
├── middleware  Echoのミドルウェア
├── openapi     oapi-codegenによって自動生成されるコード
├── repository  永続化を責務とする。DBへのクエリ実行を行う。usecaseが持つリポジトリのinterfaceを満たす。MySQL, gormに依存するのはこのパッケージのみ。
└── usecase     複数のドメインロジックを組み合わせて、実現したい一連の動作を行う。
```

### 依存関係

```
openapi
↑
controller
↓
usecase, entity
↑
repository
↓
database
```
