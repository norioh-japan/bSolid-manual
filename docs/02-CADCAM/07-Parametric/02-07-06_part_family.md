# 部品ファミリー ![部品ファミリーアイコン](../../../FIGURE/15-icone/b15b0001/PartFamily.png)

<details>
<summary>説明</summary>

部品ファミリーは、共通の特徴や機能を持ち、一部のパラメータだけが異なる一連の関連部品です。パラメトリック設計を活用することで、一つのテンプレートから様々なバリエーションの部品を効率的に作成できます。

これにより、設計の一貫性を保ちながら、異なるサイズや仕様の部品を迅速に生成できます。
</details>

<details>
<summary>関連項目</summary>

* [コントロール- キー - 指示](../_HTM_PARTI/H1-barreS-C.md#コントロール-キー-指示)
* [ビューの管理](../../../_USO-bSuiteComuni/Gestione-viste.md)
* [オブジェクトの表示方法](../../../_USO-bSuiteComuni/visualiz-oggetti.md)

**パラメトリック設計の概念：**
* [パラメータ](./02-07-01_parameters.md)
* [変数](./02-07-02_variables.md)
* [拘束条件](./02-07-03_constraints.md)
* [方程式](./02-07-04_equations.md)
* [特徴ベース設計](./02-07-05_feature_based.md)
</details>

## 部品ファミリーの基本概念

部品ファミリーは、同じ設計テンプレートに基づいて作成された一連のバリエーション部品です。各バリエーションは共通の特徴を持ちながら、サイズや一部の形状などのパラメータが異なります。

### 部品ファミリーの構成要素

#### マスターモデル
ファミリーの基本となるテンプレートモデルで、パラメータによって制御される特徴を含みます。

#### パラメータセット
ファミリー内の各バリエーションを定義するパラメータの組み合わせです。

#### ルール・制約
パラメータ間の関係や設計の整合性を保つためのルールや制約条件です。

## 部品ファミリーの作成プロセス

### 1. マスターモデルの設計

部品ファミリーの基盤となるマスターモデルを設計します。

1. モデルの基本構造と特徴を定義します。
2. 変更可能なパラメータを特定し、それらを変数として設定します。
3. パラメータ間の関係を方程式や拘束条件として定義します。

### 2. バリエーション定義

マスターモデルに基づいて、ファミリー内の各バリエーションを定義します。

1. パラメータの値のセットを作成します。
2. 各セットに名前や識別子を割り当てます。
3. 必要に応じて追加のメタデータ（材料、仕上げなど）を定義します。

### 3. テスト・検証

部品ファミリーの各バリエーションが設計要件を満たしているかを検証します。

1. 極端なパラメータ値でモデルをテストし、設計の堅牢性を確認します。
2. 製造可能性や機能的要件を評価します。
3. 必要に応じてマスターモデルや制約条件を調整します。

## 部品ファミリーの利点

### 設計の効率化
一度の設計作業で多数のバリエーションを生成できるため、設計時間が大幅に短縮されます。

### 一貫性の確保
すべてのバリエーションが同じマスターモデルに基づいているため、設計の一貫性が保たれます。

### メンテナンスの容易さ
マスターモデルを更新するだけで、ファミリー内のすべてのバリエーションに変更が反映されます。

### カスタマイズの柔軟性
顧客の要件に合わせて特定のパラメータを調整するだけで、カスタム部品を迅速に作成できます。

## 部品ファミリーの使用例

### 標準部品シリーズ
ボルト、ナット、ワッシャーなどの標準部品で、サイズやピッチが異なるバリエーションを作成します。

### 家具コンポーネント
サイズや形状が異なる棚板、引き出し、ドアなど、家具の各コンポーネントのバリエーションを管理します。

### 構造部材
長さ、幅、厚さなどのパラメータが異なる梁、柱、フレームなどの構造部材を効率的に設計します。 
