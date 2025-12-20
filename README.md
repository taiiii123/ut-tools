# ut-tools

開発・テスト業務を効率化するための統合ユーティリティツール集です。

## 概要

このリポジトリは、以下の3つの独立したプロジェクトを統合管理しています：

1. **docker-db-builder-excel** - Docker DBコンテナ構築Excelマクロ
2. **DataPrepper** - テストデータ管理Excelマクロ
3. **image-evidence-tool** - エビデンス作成Webアプリケーション

各ツールはサブモジュールとして管理されており、それぞれ独立して使用できます。

## プロジェクト一覧

### 1. docker-db-builder-excel

GUIでDockerデータベースコンテナを簡単に構築できるExcelマクロツールです。

**対応データベース:**
- MySQL
- Oracle
- PostgreSQL

**主な機能:**
- Excelシート上での設定入力
- 空きポート自動検索
- 接続情報の自動出力（A5:SQL Mk-2対応）
- コンテナの起動・停止・削除

**使用方法:**
1. `Docker_DB_Builder.xlsm` を開く
2. 必要な設定をシートに入力
3. マクロボタンでコンテナ構築

詳細は [docker-db-builder-excel](https://github.com/taiiii123/docker-db-builder-excel/tree/08bf685158f88318fa9cc4c59db910d9c769b1f3) を参照してください。

### 2. DataPrepper

テストデータをExcelで管理し、SQL文の自動生成・データベースへの直接登録ができるExcelマクロツールです。

**対応データベース:**
- MySQL
- Oracle
- PostgreSQL

**主な機能:**
- SQL INSERT/DELETE文の自動生成
- SQL文のプレビュー
- データベースへの直接登録
- バックアップ機能
- SQLファイルの自動出力

**使用方法:**
1. 対応するExcelファイルを開く（例: `MySQL/dataprepper_for_mysql.xlsm`）
2. シートにテストデータを入力
3. マクロボタンでSQL生成・実行

詳細は [DataPrepper](https://github.com/taiiii123/DataPrepper/tree/27c9024e7b10a801497ae76a44209732cb702877) を参照してください。

### 3. image-evidence-tool

テスト画像やスクリーンショットを整理し、Excel形式のエビデンス資料を簡単に作成できるWebアプリケーションです。

**主な機能:**
- 複数シート（タブ）による管理
- 画像の一括アップロード・並び替え
- 各画像へのコメント追加（説明・備考）
- Excel形式でのエビデンス出力
- 画像のライトボックス表示
- ダークモード対応
- 画像サイズ・配置のカスタマイズ

**使用方法:**
```bash
cd image-evidence-tool
npm install
npm run dev
```

詳細は [image-evidence-tool](https://github.com/taiiii123/image-evidence-tool/tree/581c3b81d1ecf0f5852167ff2d47b2a5652f1a88) を参照してください。

## セットアップ

### 各プロジェクトの要件

**docker-db-builder-excel:**
- Microsoft Excel（マクロ有効）
- Docker Desktop

**DataPrepper:**
- Microsoft Excel（マクロ有効）
- 各データベースのCLIツール（必要に応じて）

**image-evidence-tool:**
- Node.js 18以上
- npm または yarn
