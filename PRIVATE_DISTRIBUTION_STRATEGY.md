# 社内プライベートマニュアル配布戦略

## 🔒 プライベートリポジトリ対応ソリューション

GitHub Pagesが無料プランでプライベートリポジトリに対応していないため、社内用マニュアルに最適な代替案を提案します。

## 🥇 推奨ソリューション

### 1. GitBook（最推奨）⭐⭐⭐⭐⭐

**特徴**:
- ✅ **プライベート対応**: 無料プランでもプライベート空間作成可能
- ✅ **GitHub連携**: プライベートリポジトリと自動同期
- ✅ **美しいUI**: 書籍ライクなプロフェッショナルな見た目
- ✅ **強力検索**: 全文検索・タグ機能
- ✅ **チーム管理**: 社内メンバーのアクセス権限管理
- ✅ **PDF出力**: 必要時にPDF化も可能

**実装手順**:
```bash
1. GitBook.com でアカウント作成
2. プライベートスペース作成（無料）
3. GitHub integration でプライベートリポジトリ連携
4. 自動同期設定
5. チームメンバー招待
```

**コスト**: 無料〜$8/月（チーム機能）

**URL例**: `https://your-team.gitbook.io/bsolid-manual/`

### 2. MkDocs + 社内サーバー ⭐⭐⭐⭐

**特徴**:
- ✅ **完全プライベート**: 社内サーバーで運用
- ✅ **高速検索**: Lunr.js検索エンジン
- ✅ **カスタマイズ可能**: 社内ブランディング対応
- ✅ **無料**: オープンソース

**設定ファイル**:
```yaml
# mkdocs.yml
site_name: bSolid CAD/CAM 社内マニュアル
theme:
  name: material
  palette:
    primary: indigo
    accent: indigo
  language: ja
  features:
    - navigation.tabs
    - navigation.sections
    - navigation.expand
    - search.highlight
    - search.share

plugins:
  - search:
      lang: ja
  - pdf-export
```

**デプロイ方法**:
```bash
# Dockerコンテナで簡単デプロイ
docker run --rm -it -p 8000:8000 -v ${PWD}:/docs squidfunk/mkdocs-material
```

### 3. Notion Team ⭐⭐⭐⭐

**特徴**:
- ✅ **チーム専用**: プライベートワークスペース
- ✅ **リアルタイム編集**: 複数人同時編集
- ✅ **コメント機能**: セクション毎の議論
- ✅ **権限管理**: 詳細なアクセス制御

**実装手順**:
```bash
1. Notion Team プラン契約
2. Markdown一括インポート
3. ページ構造再構築
4. 社内メンバー招待・権限設定
```

### 4. Docker化Webサイト ⭐⭐⭐⭐

**特徴**:
- ✅ **完全制御**: 社内インフラで運用
- ✅ **スケーラブル**: 必要に応じて拡張
- ✅ **セキュア**: 外部アクセス完全遮断

**Dockerファイル例**:
```dockerfile
FROM nginx:alpine
COPY docs/_site /usr/share/nginx/html
COPY nginx.conf /etc/nginx/nginx.conf
EXPOSE 80
```

## 📊 比較表

| ソリューション | 導入時間 | コスト | プライベート | 検索 | 更新 | 管理 |
|----------------|----------|--------|--------------|------|------|------|
| GitBook | 30分 | 無料〜$8/月 | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | 自動 | 簡単 |
| MkDocs+サーバー | 2時間 | サーバー代 | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | 手動 | 中程度 |
| Notion | 4時間 | $8/月/人 | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ | 手動 | 簡単 |
| Docker Web | 1日 | サーバー代 | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ | 手動 | 高度 |

## 🚀 即座実装プラン：GitBook

### ステップ1: GitBook設定（15分）
```bash
1. https://www.gitbook.com/ でサインアップ
2. "Create a space" → "Private space"
3. "Import from GitHub" 選択
4. プライベートリポジトリ認証・連携
```

### ステップ2: 構造最適化（15分）
- SUMMARY.md ファイル作成で目次構造定義
- GitBookの自動同期設定
- チームメンバー招待

### ステップ3: アクセス管理（10分）
- 社内メンバーのみアクセス許可
- 読み取り専用・編集権限の設定
- 外部アクセス完全ブロック

## 📋 SUMMARY.md作成

GitBookに最適化した目次ファイルを作成しましょう：

```markdown
# Table of contents

## はじめに
* [概要](docs/01-PerIniziare/01-00_overview.md)
* [簡単な概観](docs/01-PerIniziare/01-01_breve_panoramica.md)
* [バックアップと復元](docs/01-PerIniziare/01-02_imp_back_restore.md)
* [インターフェース基本](docs/01-PerIniziare/01-03_interface_basics.md)
* [プロジェクト管理](docs/01-PerIniziare/01-04_project_management.md)

## CAD/CAM
* [概要](docs/02-CADCAM/02-00_overview.md)
* [設定](docs/02-CADCAM/02-01_configurazioni.md)
...（省略）

## トラブルシューティング
* [概要](docs/09-Troubleshooting/README.md)
* [よくある問題](docs/09-Troubleshooting/09-01_common_problems.md)
* [ネットワーク診断](docs/09-Troubleshooting/09-07_network_diagnostics.md)
* [データ復旧](docs/09-Troubleshooting/09-08_data_recovery.md)
* [高度診断](docs/09-Troubleshooting/09-09_advanced_diagnostics.md)
```

## 💡 推奨戦略

**即座実行**: GitBook（30分で完了）
1. プライベートスペース作成
2. GitHub連携設定
3. 社内チーム招待

**中期目標**: MkDocs + 社内サーバー（完全制御）
1. 社内インフラ整備
2. カスタムブランディング
3. 高度なアクセス制御

**結果**: 社内専用の美しいマニュアルサイトが即座に利用可能！ 