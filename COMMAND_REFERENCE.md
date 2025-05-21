# コマンドリファレンス

プロジェクト作業で役立つコマンド集です。随時更新していきます。

## Gitコマンド

### 基本操作

```bash
# 変更をステージングに追加
git add .                 # すべての変更を追加
git add <ファイル名>       # 特定のファイルのみ追加

# コミット
git commit -m "コミットメッセージ"  # 変更をコミット

# 状態確認
git status                # 現在の状態を確認
git log                   # コミット履歴を表示
git log --oneline         # コミット履歴を簡潔に表示
git log --oneline --decorate --graph  # グラフィカルに表示
```

### タグ操作

```bash
# タグの作成
git tag -a <タグ名> -m "タグの説明"  # 注釈付きタグを作成
git tag <タグ名>                   # 軽量タグを作成

# タグの一覧表示
git tag                   # タグ一覧
git tag -n                # 説明付きでタグ一覧を表示

# タグをリモートにプッシュ
git push origin <タグ名>   # 特定のタグをプッシュ
git push --tags           # すべてのタグをプッシュ

# タグの削除
git tag -d <タグ名>        # ローカルのタグを削除
git push origin :refs/tags/<タグ名>  # リモートのタグを削除
```

### セーブポイントへの復帰

```bash
# タグの状態に一時的に移動（閲覧のみ）
git checkout <タグ名>
# 例: git checkout v1.0-initial-backup

# 作業ブランチに戻る
git checkout master  # または git checkout main

# タグの状態に完全に戻す（注意: 現在の変更は失われます）
git reset --hard <タグ名>
# 例: git reset --hard v1.0-initial-backup

# タグの状態から新しいブランチを作成（安全な方法）
git checkout -b <新ブランチ名> <タグ名>
# 例: git checkout -b restore-branch v1.0-initial-backup
```

### リモートリポジトリ操作

```bash
# リモートの追加
git remote add origin <リポジトリURL>

# プッシュ
git push -u origin <ブランチ名>  # 初回プッシュ
git push                         # 2回目以降

# プル
git pull                         # リモートの変更を取得してマージ

# リモート情報を確認
git remote -v                    # リモートリポジトリの設定を確認
```

### ブランチ操作

```bash
# ブランチ一覧
git branch                     # ローカルブランチ一覧
git branch -a                  # リモートも含めたブランチ一覧

# ブランチ作成
git branch <ブランチ名>         # ブランチを作成
git checkout -b <ブランチ名>    # ブランチを作成して切り替え

# ブランチ切り替え
git checkout <ブランチ名>       # 指定したブランチに切り替え

# ブランチのマージ
git merge <ブランチ名>          # 現在のブランチに指定したブランチをマージ

# ブランチの削除
git branch -d <ブランチ名>      # ローカルブランチの削除
git push origin --delete <ブランチ名>  # リモートブランチの削除
```

## ターミナルコマンド（Windows PowerShell）

### ファイル操作

```powershell
# ディレクトリ内容表示
ls                        # または dir
ls -Force                 # 隠しファイルも表示

# ディレクトリ移動
cd <ディレクトリパス>       # ディレクトリを移動
cd ..                     # 親ディレクトリに移動

# ファイルやディレクトリの作成
mkdir <ディレクトリ名>      # ディレクトリを作成
New-Item -Path <ファイル名> -ItemType File  # ファイルを作成
touch <ファイル名>         # 空のファイルを作成（PowerShellのエイリアス）

# ファイルやディレクトリのコピー
cp <コピー元> <コピー先>    # ファイルをコピー
cp -r <コピー元> <コピー先>  # ディレクトリを再帰的にコピー

# ファイルやディレクトリの削除
rm <ファイル名>            # ファイルを削除
rm -r <ディレクトリ名>      # ディレクトリを再帰的に削除
rm -Force <ファイル名>      # 確認なしで削除
```

### その他の便利なコマンド

```powershell
# カレントディレクトリのパスを表示
pwd

# ファイルの内容表示
cat <ファイル名>            # ファイルの内容を表示
more <ファイル名>           # ページごとに表示

# ファイル/ディレクトリの検索
Get-ChildItem -Recurse -Filter <検索パターン>  # 再帰的に検索
# 例: Get-ChildItem -Recurse -Filter *.md      # すべての.mdファイルを検索

# ファイル内のテキスト検索
Select-String -Path <ファイルパス> -Pattern <検索パターン>
# 例: Select-String -Path *.md -Pattern "Git"  # すべての.mdファイル内でGitを検索
```

## bSolid-manualプロジェクト特有のコマンド

### チェックアウトポイント

```bash
# v1.0-initial-backup（Gitタグ）にチェックアウト
git checkout v1.0-initial-backup

# マスターブランチに戻る
git checkout master
```

---

このリファレンスファイルは随時更新していきます。必要なコマンドがあれば追加してください。 