# bSolid マニュアル - 2つのセクションおよび1つの閉じたパスからの面

![2つのセクションおよび1つの閉じたパスからの面アイコン](../../../FIGURE/15-icone/b15b0001/Draw_Solid_1Plant2Section.png)

## 説明

以下の形状エレメントを結合することによって面を作成します。

- 上から見た面の平面図を表す閉じた形状図形。
- 基準セグメントとともにオブジェクトの形を決める2つのフリーでオープンアウトライン。
- 2つの基準セグメントで、その拡張が閉じた形状図形をはさみ取らなければならないもの。セグメントは、面の平面図に垂直な2つの平面を形成するための基準です。2つのセグメントがはさみ取る点は、2つの平面がはさみ取る頂点です。

![1つの平面上に構成される面の例](../../../FIGURE/08/arte4-D/d08t0196.png)

**A.** 閉じた形状図形；形状のパス  
**B.** フリーでオープンアウトライン：第1セクション、第2セクション  
**C.** 基準セグメント：第一基準線；第二基準線

## 関連項目

- [より高度な形状用のタブ](../../04-Geo2D/README.md) - より高度な形状作成オプション
- [コントロール- キー - 指示](../_HTM_PARTI/H1-barreS-C.md#コントロール-キー-指示)
- [ビューの管理](../../../_USO-bSuiteComuni/Gestione-viste.md)
- [オブジェクトの表示方法](../../../_USO-bSuiteComuni/visualiz-oggetti.md)
- [平面図形または3D図形を作成する](../02-Nozioni/Dis-figure.md#平面図形または3D図形を作成する)

### 描画の概念

- [構成平面](../02-Nozioni/PianoCostr.md#構成平面)
- [平面図形または3D図形を作成する](../02-Nozioni/Dis-figure.md#平面図形または3D図形を作成する)
- [オブジェクトを操作する](../02-Nozioni/oggetti.md#オブジェクトを操作する)
- [カーソルの動きの制限および妨害](../02-Nozioni/puntatore.md#カーソルの動きの制限および妨害)

## 教育ビデオへのリンク

- [3次元のフィギュアの作成](../09-VIDEO.md)

## セクション一覧

- [形状を選択する](#形状を選択する)
- [モード](#モード)
- [プロパティ](../../04-Geo2D/README.md#プロパティ)
- [繰り返し](../../04-Geo2D/README.md#繰り返し)
- [CAMデータ](../../04-Geo2D/README.md#CAMデータ)

## 形状を選択する

### 形状のパス
**パラメーター:** PLT

面のレイアウトを表す閉じた形状図形を選択するために使用されます。

### 第1セクション
**パラメーター:** SEC1

最初のオープンアウトラインを選択して面の第1セクションを作成するために使用されます。

### 第2セクション
**パラメーター:** SEC2

2番目のオープンアウトラインを選択して面の第2セクションを作成するために使用されます。

### 第一基準線
**パラメーター:** LIN1

第1セクションと一緒に面の第一基準線を作成するオープンセグメントを選択するために使用されます。

### 第二基準線
**パラメーター:** LIN2

第2セクションと一緒に面の第二基準線を作成するオープンセグメントを選択するために使用されます。

## モード

### 凹面
**パラメーター:** CV

作成した面の凹面のタイプを選択するために使用されます。

#### ![凹面](../../../FIGURE/15-icone/b15b0001/Draw_Solid_Concave.png) 凹面

面を凹面にします。

#### ![凸面](../../../FIGURE/15-icone/b15b0001/Draw_Solid_Concave.png) 凸面

面を凸面にします。

### 精度
**パラメーター:** PR

作成した3Dの図の精密さを定義するインデックス。1000より小さい値にするとオブジェクトがより精密になる。

## 関連項目

- [形状用のタブ](../../04-Geo2D/README.md) - より高度な形状作成オプション
- [3次元のフィギュアの作成](../README.md) - 3Dモデリングの概要
- [基本立体](./02-06-01_solid_primitives.md) - 基本的な3D形状の作成
- [押し出し](./02-06-02_extrusion.md) - 2D形状からの押し出し
- [回転](./02-06-03_revolution.md) - 回転による立体作成
- [セクションからの面](./02-06-05_loft.md) - セクションからの面の作成

## 上位セクションに戻る

- [3D図形](./README.md)
- [CAD/CAM](../README.md)
- [bSolid マニュアル目次へ戻る](../../README.md) 
