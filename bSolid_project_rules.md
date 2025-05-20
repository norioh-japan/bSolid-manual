# bSolid Project Rules

> **継承宣言**> 本プロジェクトは Cursor の **User Rules**（`# 基本指示.txt`）を継承します。ここでは *追加ルール* と *上書き（Override）* のみを定義します。

---

## 1. ソース範囲

- 開始フォルダ: `01-PerIniziare`。順次 `02-CADCAM`, `03-…` と展開。
- HTML・画像・Glossary・JavaScript など、元ヘルプに含まれるすべてのファイルをワークスペースに追加。

## 2. 出力フォーマット

| 対象     | 形式                            | 備考                       |
| ------ | ----------------------------- | ------------------------ |
| 主原稿    | **Markdown (.md)**            | Git でバージョン管理。h4 見出しまで展開。 |
| 補足テキスト | `<details>` 折りたたみ             | クリック / タップで展開。           |
| 画像     | PNG (UI), WebP80% (写真)        | `srcset` で 1× / 2× 提供。   |
| 翻訳メモリ  | TMX (`docs/tm/bsolid_jp.tmx`) | Glossary は CSV。          |

## 3. 抽出粒度

- **1 段落 = 1 セグメント** で Markdown に出力。
- 手順番号・原文ステップを 1:1 で保持。
- UI ラベルは原文英語 + 日本語対訳を併記。

## 4. 用語集 / 翻訳メモリ

- Glossary ファイル: `docs/tm/glossary.csv`（列: EN, JA, Note）。
- TMX ファイルに対訳を蓄積し、CAT ツール連携必須。
- CI で `tm‑lint` を実行し、Glossary 不一致は **Fail** とする。

## 5. 補足ポップアップ処理

| 文字数    | 表示方法              |
| ------ | ----------------- |
| 〜30 字  | 脚注 (`[^1]`)       |
| 31 字以上 | `<details>` 折りたたみ |

## 6. 画像規格

| 項目      | 値                                                        |
| ------- | -------------------------------------------------------- |
| 原本キャプチャ | 横 ≥ **1920 px** (PNG24)                                  |
| 配布サイズ   | 960 px (`@1x`), 1920 px (`@2x`)                          |
| 命名規則    | `{chapter}-{section}_stepXX.png` (例: `01-02_step05.png`) |
| 代替テキスト  | UI 名称 + 状態説明（日本語）                                        |
| 画像ソース   | **必ず元ドキュメント（Help/ja/5804sb0002/）から直接コピー**。代替は最終手段。       |
| 画像パス    | 元と同じ相対構造で `FIGURE/{カテゴリ}/{グループ}/` に配置                   |

## 7. ディレクトリ / ファイル命名

```
📂 docs
 ├─ 01-PerIniziare
 │   ├─ img
 │   │   ├─ 01-00_step01@1x.png
 │   │   └─ 01-00_step01@2x.png
 │   └─ 01-00_overview.md
 ├─ 02-CADCAM
 └─ tm
     ├─ bsolid_jp.tmx
     └─ glossary.csv
```

## 8. レビュー & Pull Request フロー

1. **Draft PR** で目次案 / 抽出結果を提出。
2. Reviewer がチェックし、コメント反映。
3. CI (Markdown‑lint, tm‑lint, image‑lint) が Pass。
4. **Squash merge** で main ブランチへ。

## 9. 変更履歴

- `CHANGELOG.md` に Semantic Versioning で記載： `v0.1.0` (outline), `v0.2.0` (details)…

## 10. ライセンス & 著作権

- 教育・社内利用を前提。社外公開時は Biesse S.p.A. ライセンス条項を確認。
- ロゴ画像使用はブランドガイドラインに従うこと。

---

### 付録 A ― CI 例 (GitHub Actions)

```yaml
name: docs‑ci
on: [pull_request]
jobs:
  lint:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: TM Lint
        run: npx tm-lint docs/**/*.md --tm docs/tm/bsolid_jp.tmx
      - name: Markdown Lint
        run: npx markdownlint-cli "docs/**/*.md"
```