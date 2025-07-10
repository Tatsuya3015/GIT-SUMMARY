# 📝 Git & GitHub 活用の基本ステップまとめ（CLI不要版）

## ✅ 1. Gitの初期準備（1回だけでOK）

▶ Gitがインストールされているか確認：
```bash
git --version
# 出力例：git version 2.39.5
```

## ✅ 2. 新しいプロジェクトの作成とGit管理の開始

```bash
mkdir プロジェクト名       # 新しいプロジェクト用のフォルダを作成
cd プロジェクト名          # フォルダに移動
git init                   # Gitでの履歴管理を開始（初期化）
```

### 📂 ディレクトリの移動方法

```bash
# 現在のディレクトリを確認
pwd

# ディレクトリを移動する方法
cd ディレクトリ名          # 指定したディレクトリに移動
cd ..                     # 一つ上のディレクトリに移動
cd ~                      # ホームディレクトリに移動

# ディレクトリの内容を確認
ls                        # ファイルとディレクトリの一覧を表示
ls -la                    # 隠しファイルも含めて詳細表示
```

### ⚠️ 注意：ルートディレクトリへの移動について

```bash
cd /                      # ルートディレクトリに移動（⚠️ 注意が必要）
```

**なぜ注意が必要？**
- ルートディレクトリ（`/`）はシステム全体の最上位ディレクトリ
- 誤って重要なシステムファイルを削除するリスクがある
- 初心者の方は避けることを推奨

**安全な代替方法：**
```bash
cd ~                      # ホームディレクトリに移動（推奨）
cd ~/Desktop              # デスクトップに移動
cd ~/Documents            # ドキュメントフォルダに移動
```

## ✅ 3. ファイルを作って履歴に記録する

```bash
echo "<h1>Hello Git</h1>" > index.html   # サンプルファイル作成
git add .                                # すべての変更をステージング
git commit -m "初回コミット"             # 履歴に記録（コミット）
```

## ✅ 4. GitHubアカウントを確認／作成（1回だけ）

- https://github.com/login からログイン
- アカウントがない場合は https://github.com/signup で作成

## ✅ 5. GitHubでリポジトリを作成

1. GitHubにログイン
2. 左上の【Create repository】をクリック
3. 以下のように入力：
   - Repository name：例 my-first-repo
4. 公開/非公開：どちらでもOK
5. ☑️ Initialize with README → チェックしない
6. [Create repository] ボタンをクリック

## ✅ 6. GitHubリポジトリとローカルプロジェクトを接続

ターミナルでローカルプロジェクトの中にいる状態で：
```bash
git remote add origin https://github.com/あなたのユーザー名/リポジトリ名.git
git branch -M main      # 初回のみ
```

## ✅ 7. GitHubにアップロード（Push）

```bash
git push -u origin main
# 初回のみログイン確認（ブラウザ連携 or トークン）が出る場合あり
```

## ✅ 8. 成功したら確認！

GitHub上のリポジトリページを開く
アップロードされたファイルとコミット履歴が表示されていれば成功🎉

## ✅ よく使うGitコマンド一覧

| 操作 | コマンド |
|------|----------|
| 状態確認 | `git status` |
| 履歴確認 | `git log` |
| 差分確認 | `git diff` |
| ファイル戻す | `git restore ファイル名` |
| ステージング | `git add .` |
| 履歴に記録 | `git commit -m "メッセージ"` |
| GitHubに送信 | `git push` |

## 🧠 GitとGitHubの違い

- **Git**：ローカルで履歴を管理
- **GitHub**：クラウドで共有・保存・公開
- 使い分け：一人で使うならGitだけでもOK、チームや公開ならGitHubと連携

## 🧠 補足：GitHubはいつ使うべき？

- ✔ バックアップをとりたいとき
- ✔ 他人と共有・チーム開発するとき
- ✔ ポートフォリオとして公開したいとき

## 📌 重要ポイントまとめ

- プロジェクトごとにディレクトリ＋Git初期化が基本
- GitHub連携は必要なときだけでOK
- 1つのプロジェクトに対し1つのリポジトリが原則
- Gitはローカル履歴管理、GitHubはクラウド共有ツール

> **注意**: Command+S（ファイルの保存）をしていなければ、git add → commit → push しても、その変更内容はGitにもGitHubにも反映されません。

### 基本的な作業の流れ

1. 編集（エディタ上）
2. ✅ 保存（Command+S）
3. `git add`
4. `git commit`
5. `git push`

## 🤝 リポジトリを友人に共有する方法

### 1. GitHubでリポジトリを公開する場合

1. GitHubのリポジトリページにアクセス
2. Settingsタブをクリック
3. 「Danger Zone」セクションまでスクロール
4. 「Change repository visibility」をクリック
5. 「Make public」を選択
6. リポジトリ名を入力して確認
7. 共有したい友人にリポジトリのURLを送信

### 2. 友人をコラボレーターとして追加する場合

1. GitHubのリポジトリページにアクセス
2. Settingsタブをクリック
3. 左サイドバーの「Collaborators and teams」をクリック
4. 「Add people」ボタンをクリック
5. 友人のGitHubユーザー名またはメールアドレスを入力
6. 権限レベルを選択（通常は「Write」推奨）
7. 「Add [ユーザー名] to this repository」をクリック

### 3. 友人側での作業手順

友人に以下の手順を共有してください：

```bash
# リポジトリをクローン（初回のみ）
git clone https://github.com/あなたのユーザー名/リポジトリ名.git

# クローンしたディレクトリに移動
cd リポジトリ名

# ファイルを編集・保存

# 変更をGitに追加
git add .

# 変更をコミット
git commit -m "変更内容の説明"

# GitHubにプッシュ
git push origin main
```

### 4. 共有時の注意点

- **公開リポジトリ**: 誰でも見ることができる（推奨）
- **プライベートリポジトリ**: 招待した人のみアクセス可能
- **コラボレーター追加**: 友人に編集権限を与える場合
- **URL共有**: 読み取り専用で共有したい場合

### 5. リポジトリのURLを確認する方法

```bash
# リモートリポジトリのURLを確認
git remote -v
```

出力例：
```
origin  https://github.com/ユーザー名/リポジトリ名.git (fetch)
origin  https://github.com/ユーザー名/リポジトリ名.git (push)
```