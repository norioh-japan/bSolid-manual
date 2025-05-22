# bSolid ドキュメンテーションプロジェクト

このリポジトリには、Biesse社のbSolidソフトウェアの日本語ドキュメントが含まれています。

## プロジェクト構造

```
📂 docs
 ├─ 01-PerIniziare
 │   ├─ img
 │   ├─ README.md
 │   ├─ 01-00_overview.md
 │   ├─ 01-01_breve_panoramica.md
 │   └─ 01-02_imp_back_restore.md
 ├─ 02-CADCAM
 │   ├─ 04-Geo2D
 │   │   ├─ 02-04-01_point.md
 │   │   ├─ 02-04-02_line.md
 │   │   ├─ 02-04-03_circle.md
 │   │   ├─ 02-04-04_arc.md
 │   │   ├─ 02-04-05_ellipse.md
 │   │   ├─ 02-04-06_polygon.md
 │   │   └─ 02-04-07_spline.md
 │   ├─ 05-Modifica
 │   │   ├─ 02-05-01_transform.md
 │   │   ├─ 02-05-02_modify.md
 │   │   └─ 02-05-03_dimension.md
 │   ├─ 06-Geo3D
 │   │   ├─ 02-06-01_solid_primitives.md
 │   │   ├─ 02-06-02_extrusion.md
 │   │   ├─ 02-06-03_revolution.md
 │   │   ├─ 02-06-04_sweep.md
 │   │   ├─ 02-06-05_loft.md
 │   │   └─ 02-06-06_boolean.md
 │   ├─ 07-Parametric
 │   │   ├─ 02-07-01_parameters.md
 │   │   ├─ 02-07-02_variables.md
 │   │   ├─ 02-07-03_constraints.md
 │   │   ├─ 02-07-04_equations.md
 │   │   ├─ 02-07-05_feature_based.md
 │   │   └─ 02-07-06_part_family.md
 │   ├─ README.md
 │   ├─ 09-VIDEO.md
 │   ├─ 02-00_overview.md
 │   ├─ 02-01_configurazioni.md
 │   ├─ 02-02_cad-tastiMouse.md
 │   └─ 02-03_pianoCostr.md
 ├─ 03-SimMacchina
 │   ├─ README.md
 │   ├─ 03-00_overview.md
 │   ├─ 03-01_Macc-presentaz.md
 │   ├─ 03-02_Macc-struttura01.md
 │   └─ 03-03_Macc-UsoAmbiente.md
 ├─ 04-RegolebSolid
 │   ├─ README.md
 │   ├─ 04-00_overview.md
 │   ├─ 04-01_esplorare.md
 │   ├─ 04-02_dati-catalog.md
 │   └─ 04-03_Uso-reg.md
 ├─ 05-Utensili
 │   ├─ README.md
 │   ├─ 05-00_overview.md
 │   ├─ 05-01_esplorare.md
 │   ├─ 05-02_dati-catalog.md
 │   └─ 05-03_Uso-reg.md
 ├─ 06-Impostaz
 │   ├─ README.md
 │   ├─ 06-00_overview.md
 │   ├─ 06-01_Impost-general.md
 │   ├─ 06-02_datiUtente.md
 │   ├─ 06-03_sincronizzazione.md
 │   ├─ 06-04_distinta.md
 │   ├─ 06-05_datiTaglio.md
 │   ├─ 06-06_Lavorazioni.md
 │   └─ 06-07_barcode.md
 ├─ 07-Distinte
 │   ├─ README.md
 │   ├─ 07-00_overview.md
 │   ├─ 07-01_presentazione.md
 │   ├─ 07-02_utilizzo.md
 │   ├─ 07-03_strumenti.md
 │   └─ 07-04_barcode.md
 ├─ 08-Attrezzaggio
 │   ├─ README.md
 │   ├─ 08-00_overview.md
 │   ├─ 08-01_presentazione.md
 │   ├─ 08-02_struttura.md
 │   ├─ 08-03_utilizzo.md
 │   └─ 08-04_strumenti.md
 ├─ 09-Troubleshooting
 │   └─ README.md
 └─ tm
     ├─ bsolid_jp.tmx
     └─ glossary.csv
```

## 進捗状況

- [x] プロジェクト初期構造の設定
- [x] 01-PerIniziare（始めるために）セクションの基本ファイル変換
  - [x] 短い説明 
  - [x] リセット-機械データ保存
  - [x] インターフェイスの基本
  - [x] プロジェクト管理
  - [x] READMEファイルの追加
  - [ ] その他のファイル
- [x] 02-CADCAM セクションの基本構造作成
  - [x] 環境設定
  - [x] マウスのキーを使用する
  - [x] 構成平面
  - [x] 2Dジオメトリ
    - [x] 点
    - [x] 線
    - [x] 円
    - [x] 円弧
    - [x] 楕円
    - [x] 多角形
    - [x] スプライン
  - [x] 図形操作・編集
    - [x] 変換操作
    - [x] 変形操作
    - [x] 寸法と注釈
  - [x] 3Dモデリング
    - [x] 基本立体
    - [x] 押し出し
    - [x] 回転体
    - [x] スイープ
    - [x] ロフト
    - [x] ブール演算
  - [x] パラメトリックデザイン
    - [x] パラメータ
    - [x] 変数
    - [x] 拘束条件
    - [x] 方程式
    - [x] 特徴ベース設計
    - [x] 部品ファミリー
  - [x] 教育ビデオ
    - [x] 3次元のフィギュアの作成
    - [x] プログラミング
  - [x] READMEファイルの追加
  - [ ] その他のファイル
- [x] 他のセクションの変換
  - [x] 03-SimMacchina（機械シミュレーション）セクション
    - [x] 基本構造の作成
    - [x] 個別ファイルの変換
      - [x] 機械シミュレーション紹介
      - [x] 機械構造
      - [x] 環境の使用
    - [x] READMEファイルの追加
  - [x] 04-RegolebSolid（bSolidルール）セクション
    - [x] 基本構造の作成
    - [x] 個別ファイルの変換
      - [x] ルールの探索
      - [x] データカタログ
      - [x] ルールの使用
    - [x] READMEファイルの追加
  - [x] 05-Utensili（ツール）セクション
    - [x] 基本構造の作成
    - [x] 個別ファイルの変換
      - [x] ツールの探索
      - [x] データカタログ化
      - [x] ツールの使用
    - [x] READMEファイルの追加
  - [x] 06-Impostaz（設定）セクション
    - [x] 基本構造の作成
    - [x] 個別ファイルの変換
      - [x] 一般設定
      - [x] ツールデータ
      - [x] 同期
      - [x] リスト
      - [x] 切断データ
      - [x] 加工作業
      - [x] バーコード
    - [x] READMEファイルの追加
  - [x] 07-Distinte（リスト）セクション
    - [x] 基本構造の作成
    - [x] 個別ファイルの変換
      - [x] リストの紹介
      - [x] リストの使用方法
      - [x] ツールリスト
      - [x] バーコードの使用
    - [x] READMEファイルの追加
  - [x] 08-Attrezzaggio（装備）セクション
    - [x] 基本構造の作成
    - [x] 個別ファイルの変換
      - [x] 装備の紹介
      - [x] 装備の構造
      - [x] 装備の使用方法
      - [x] 装備ツール
    - [x] READMEファイルの追加
  - [x] 09-Troubleshooting（トラブルシューティング）セクション
    - [x] 基本構造の作成
    - [x] READMEファイルの追加（よくある問題と解決方法）

## プロジェクトルール

このプロジェクトは [bSolid_project_rules.md](bSolid_project_rules.md) に従って運用されます。主なルールには以下が含まれます：

1. ソース範囲
2. 出力フォーマット
3. 抽出粒度
4. 用語集/翻訳メモリ
5. 補足ポップアップ処理
6. 画像規格
7. ディレクトリ/ファイル命名
8. レビュー & Pull Request フロー
9. 変更履歴
10. ライセンス & 著作権

詳細は [bSolid_project_rules.md](bSolid_project_rules.md) を参照してください。

## 貢献方法

1. このリポジトリをフォークする
2. 変更を行うブランチを作成する (`git checkout -b feature/your-feature`)
3. 変更をコミットする (`git commit -am 'Add some feature'`)
4. ブランチにプッシュする (`git push origin feature/your-feature`)
5. Pull Requestを作成する

## ライセンス

教育・社内利用を前提としています。社外公開時はBiesse S.p.A.のライセンス条項を確認してください。 