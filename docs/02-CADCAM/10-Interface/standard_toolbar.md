# 標準バー

**ファイル名**: `standard_toolbar.md`  
**カテゴリ**: インターフェース - 標準バー

## 概要

標準バーは、bSolidアプリケーションの最上部に位置するメインツールバーです。CAD/CAM環境で最も頻繁に使用される基本機能へのクイックアクセスを提供し、効率的なワークフローの基盤となります。このバーは5つの主要セクションに分かれており、プロジェクト管理から視覚化まで、幅広い機能をカバーしています。

![標準バー](../../Help/ja/5804sb0002/FIGURE/05/arte4/b05b0652-P.png)

## 標準バーの構成

標準バーは以下の5つのセクションで構成されています：

| セクション | 内容 | 主な機能 |
|-----------|------|----------|
| **A. 一般的ツール** | ファイル操作と基本編集 | 新規作成、保存、コピー、貼り付け等 |
| **B. 表示管理ツール** | 画面表示の操作 | 選択、回転、ズーム、パン等 |
| **C. 直交ビューツール** | 標準視点からの表示 | 正面、側面、上面等の切り替え |
| **D. 方向ツール** | 表示方向の調整 | 任意角度からの視点設定 |
| **E. 表示ツール** | オブジェクトの表示方法 | ワイヤーフレーム、写実的、メッシュ表示 |

## A. 一般的ツール

### ファイル操作ツール

#### 新規作成
![新規アイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/File_New.png)

**機能**: 新しいbSolidドキュメントを作成  
**ショートカット**: **Ctrl + N**

**操作手順**:
1. 新規ボタンをクリック
2. プロジェクトタイプを選択（2D/3D、材料等）
3. 基本設定を確認
4. 作業開始

**新規作成オプション**:
- **空白ドキュメント**: 何もない状態から開始
- **テンプレート使用**: 事前定義された設定から開始
- **ウィザード使用**: ガイド付きプロジェクト作成

#### 開く
![開くアイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/File_Open.png)

**機能**: 既存のbSolidドキュメントを開く  
**ショートカット**: **Ctrl + O**

**対応ファイル形式**:
- **.bSolid**: bSolid標準形式
- **.dxf/.dwg**: AutoCAD形式
- **.step/.iges**: 3D CAD標準形式
- **その他**: 各種CAD形式

#### 保存
![保存アイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/File_Save.png)

**機能**: 現在のドキュメントを保存  
**ショートカット**: **Ctrl + S**

**保存の種類**:
- **上書き保存**: 既存ファイルを更新
- **新規保存**: 初回保存時はファイル名を指定
- **自動保存**: 設定された間隔で自動実行

#### 名前を付けて保存
![名前を付けて保存アイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/File_SaveAs.png)

**機能**: 現在のドキュメントのコピーに新しい名前を付けて保存

**活用場面**:
- **バージョン管理**: 設計の段階的な保存
- **バックアップ作成**: 重要な節目での保存
- **派生版作成**: 基本設計からの変更版作成

#### マクロとして保存
![マクロ保存アイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/File_SaveAsMacro.png)

**機能**: 現在の作業手順をマクロとして保存

**マクロの活用**:
- **作業効率化**: 繰り返し作業の自動化
- **品質統一**: 標準化された手順の保証
- **ノウハウ蓄積**: 熟練者の技術の保存と共有

### インポート・エクスポート

#### インポート
![インポートアイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/File_Import.png)

**機能**: 各種形式のファイルを現在のドキュメントにインポート  
**ショートカット**: **Ctrl + I**

**対応形式**:
- **DXF/DWG**: AutoCAD形式の2D図面
- **STL**: 3Dプリント用メッシュデータ
- **STEP/IGES**: 3D CAD標準形式
- **BMP/JPG**: 画像ファイル（トレース用）

#### エクスポート
![エクスポートアイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/File_Export.png)

**機能**: 現在のドキュメントデータを他形式で保存  
**ショートカット**: **Ctrl + E**

**出力形式**:
- **DXF/DWG**: AutoCAD互換形式
- **STL**: 3Dプリント用
- **CIX**: CAM用加工データ
- **PDF**: 図面印刷用

#### 印刷
![印刷アイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/File_Print.png)

**機能**: 現在のドキュメントを印刷  
**ショートカット**: **Ctrl + P**

### 編集操作ツール

#### 切り取り
![切り取りアイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/Edit_Cut.png)

**機能**: 選択したオブジェクトを切り取り  
**ショートカット**: **Ctrl + X**

**動作説明**:
- 選択オブジェクトをクリップボードに保存
- 元の位置からは削除（視覚的に非表示）
- 貼り付けまで一時的に保持

#### コピー
![コピーアイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/Edit_Copy.png)

**機能**: 選択したオブジェクトをコピー  
**ショートカット**: **Ctrl + C**

#### 貼り付け
![貼り付けアイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/Edit_Paste.png)

**機能**: 切り取り/コピーしたオブジェクトを貼り付け  
**ショートカット**: **Ctrl + V**

#### 削除
![削除アイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/Edit_Delete.png)

**機能**: 選択したオブジェクトを完全削除  
**ショートカット**: **Delete**

**注意事項**:
- 削除は完全な除去（切り取りとは異なる）
- 削除後は「元に戻す」でのみ復旧可能

#### 元に戻す
![元に戻すアイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/File_Undo.png)

**機能**: 最後に実行した作業を取り消し  
**ショートカット**: **Ctrl + Z**

#### やり直し
![やり直しアイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/File_Redo.png)

**機能**: 取り消した操作を復元  
**ショートカット**: **Ctrl + Y**

#### UCS面
![UCS面アイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/View_UCSFace.png)

**機能**: 選択した非標準面を基準として構築面を設定  
**ショートカット**: **Ctrl + Alt + 6**

## B. 表示管理ツール

### 基本選択・操作ツール

#### オブジェクト選択
![選択アイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/Selection_Selection_Select.png)

**機能**: オブジェクトを選択するための十字カーソルをアクティブ化

**選択方法**:
- **単一選択**: クリックで1個のオブジェクトを選択
- **複数選択**: Ctrlキーを押しながらクリックで追加選択
- **範囲選択**: ドラッグで矩形範囲内の全オブジェクトを選択

#### ビュー回転
![回転アイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/View_Rotations.png)

**機能**: 3Dビューを回転させるカーソルモードをアクティブ化

#### パン（移動）
![パンアイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/View_Pan.png)

**機能**: ビューを移動するパンコマンドをアクティブ化  
**ショートカット**: **Ctrl + Alt + W**

### ズーム操作ツール

#### 拡大
![拡大アイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/View_ZoomPlus.png)

**機能**: 描画エリアの表示を拡大  
**ショートカット**: **Page Up**

#### 縮小
![縮小アイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/View_ZoomMinus.png)

**機能**: 描画エリアの表示を縮小  
**ショートカット**: **Page Down**

#### 全体表示
![全体表示アイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/View_ZoomAll.png)

**機能**: 全ての作成済みオブジェクトを画面に収める  
**ショートカット**: **Home**

#### 選択表示
![選択表示アイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/View_ZoomObjects.png)

**機能**: 選択したオブジェクトのみを画面に収める  
**ショートカット**: **End**

## C. 直交ビューツール

### 標準視点ツール

#### 平面図（上面図）
![平面図アイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/View_Plane.png)

**機能**: 上方からの垂直俯瞰ビュー  
**ショートカット**: **Ctrl + 1**

#### 正面図
![正面図アイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/View_Front.png)

**機能**: 正面からの水平ビュー  
**ショートカット**: **Ctrl + 2**

#### 右側面図
![右側面図アイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/View_RightSide.png)

**機能**: 右側面からのビュー  
**ショートカット**: **Ctrl + 3**

#### 背面図
![背面図アイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/View_Back.png)

**機能**: 背面からのビュー  
**ショートカット**: **Ctrl + 4**

#### 左側面図
![左側面図アイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/View_LeftSide.png)

**機能**: 左側面からのビュー  
**ショートカット**: **Ctrl + 5**

#### 底面図
![底面図アイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/View_Bottom.png)

**機能**: 下方からの仰視ビュー  
**ショートカット**: **Ctrl + 6**

## D. 方向ツール

### 3D視点制御

#### アイソメトリックビュー
![アイソメトリックアイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/View_Isometric.png)

**機能**: 3次元の等角投影ビュー  
**ショートカット**: **Ctrl + 8**

**特徴**:
- **等角投影**: X、Y、Z軸が等角度で表示
- **立体感**: 3次元形状の理解に最適
- **設計確認**: 全体的な形状確認に使用

#### 透視図法ビュー
![透視図法アイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/View_Perspective.png)

**機能**: 遠近法による立体視ビュー  
**ショートカット**: **Ctrl + 9**

#### フリービュー
![フリービューアイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/View_Free.png)

**機能**: 任意の角度からの自由視点  
**ショートカット**: **Ctrl + 0**

## E. 表示ツール

### 表示モード切り替え

#### ワイヤーフレーム表示
![ワイヤーフレームアイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/View_Wireframe.png)

**機能**: 3D図形をワイヤーフレーム（線画）で表示

**特徴**:
- **高速表示**: 計算負荷が軽く、滑らかな操作
- **構造理解**: 内部構造や重なり部分の確認
- **編集作業**: 頂点や辺の選択・編集に適している

#### 写実的表示
![写実的表示アイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/View_Photorealistic.png)

**機能**: 3D図形を色と影付きで現実的に表示

**特徴**:
- **材質表現**: 木材、金属、プラスチック等の質感
- **照明効果**: 光源による陰影とハイライト
- **立体感**: 奥行きと形状の理解向上

**活用場面**:
- **プレゼンテーション**: 顧客への提案・説明
- **品質確認**: 最終製品の外観確認
- **カタログ作成**: 製品画像の作成

#### メッシュ表示
![メッシュ表示アイコン](../../Help/ja/5804sb0002/FIGURE/15-icone/b15b0001/View_Mesh.png)

**機能**: 3D図形の三角メッシュ構造を表示

**用途**:
- **内部構造確認**: プロファイルラインの視覚化
- **隠線表示**: 通常見えない内部の線や円弧
- **メッシュ品質確認**: 3Dモデルの面分割状況

## 効率的な標準バー活用法

### ワークフロー別推奨ツール

#### 設計初期段階
1. **新規作成** → **アイソメトリックビュー** → **ワイヤーフレーム表示**
2. **全体表示** → **フリービュー** → **選択ツール**

#### 詳細設計段階
1. **直交ビュー切り替え** → **拡大/縮小** → **パン操作**
2. **コピー/貼り付け** → **元に戻す/やり直し**

#### プレゼンテーション
1. **写実的表示** → **透視図法** → **回転操作**
2. **全体表示** → **印刷/エクスポート**

### 重要ショートカット

**最重要ショートカット**:
- **Ctrl + S**: 保存（頻繁に使用）
- **Ctrl + Z**: 元に戻す（失敗時の復旧）
- **Home**: 全体表示（迷子時の復帰）
- **Page Up/Down**: 拡大/縮小（詳細確認）

**ビュー切り替え系**:
- **Ctrl + 1～6**: 各直交ビュー
- **Ctrl + 8**: アイソメトリック
- **Ctrl + 9**: 透視図法
- **Ctrl + 0**: フリービュー

## トラブルシューティング

### よくある問題と解決法

#### ツールバーが見えない
**対処法**:
- メニューから「表示」→「ツールバー」→「標準バー」をチェック
- ウィンドウサイズの調整、またはツールバーの再配置

#### ショートカットが機能しない
**確認項目**:
- IMEの状態確認（英語入力にする）
- 他のアプリケーションとのキー競合
- ショートカット設定の確認・再設定

#### 操作が重い・遅い
**改善方法**:
- ワイヤーフレーム表示への切り替え
- 使用可能メモリの確認
- プロジェクトファイルの最適化

## 関連セクション

- [ショートカットキー](./shortcuts.md) - キーボード操作との連携
- [マウス操作](./mouse_operations.md) - マウス操作との組み合わせ
- [ステータスバー](./status_bar.md) - ステータス表示との連携
- [インターフェース概要](./interface_overview.md) - 全体構成の理解

## 上位セクションへ戻る

- [インターフェース](./README.md) - インターフェースセクション目次
- [CAD/CAM](../README.md) - CAD/CAMセクション目次
- [bSolid マニュアル目次](../../README.md) - メイン目次

---

**注意**: 標準バーの機能の一部は、使用しているライセンスや環境設定により利用できない場合があります。ショートカットキーは日本語入力がOFFの状態で使用してください。頻繁に使用する機能は積極的にショートカットキーを活用することで、作業効率が大幅に向上します。 
