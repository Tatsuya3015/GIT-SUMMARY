# 📝 Git & GitHub 活用の基本ステップまとめ（CLI不要版）

##✅ 1. Gitの初期準備（1回だけでOK）
▶ Gitがインストールされているか確認：
bash
git --version
出力例：git version 2.39.5

---

##✅ 2. 新しいプロジェクトの作成とGit管理の開始
bash
mkdir プロジェクト名       # 新しいプロジェクト用のフォルダを作成
cd プロジェクト名          # フォルダに移動
git init                   # Gitでの履歴管理を開始（初期化）

---

##✅ 3. ファイルを作って履歴に記録する
bash
cho "<h1>Hello Git</h1>" > index.html   # サンプルファイル作成
git add .                                # すべての変更をステージング
git commit -m "初回コミット"             # 履歴に記録（コミット）

---

##✅ 4. GitHubアカウントを確認／作成（1回だけ）
https://github.com/login からログイン
アカウントがない場合は https://github.com/signup で作成

---

##✅ 5. GitHubでリポジトリを作成
1.GitHubにログイン
2.左上の【Create repository】をクリック
3.以下のように入力：Repository name：例 my-first-repo
4.公開/非公開：どちらでもOK
5.☑️ Initialize with README → チェックしない
6.[Create repository] ボタンをクリック

---

##✅ 6. GitHubリポジトリとローカルプロジェクトを接続
ターミナルでローカルプロジェクトの中にいる状態で：
bash
git remote add origin https://github.com/あなたのユーザー名/リポジトリ名.git
git branch -M main      # 初回のみ

---

##✅ 7. GitHubにアップロード（Push）
bash
git push -u origin main
初回のみログイン確認（ブラウザ連携 or トークン）が出る場合あり

---

##✅ 8. 成功したら確認！
GitHub上のリポジトリページを開く
アップロードされたファイルとコミット履歴が表示されていれば成功🎉

---

##✅ よく使うGitコマンド一覧
| 操作             | コマンド                     |
|------------------|------------------------------|
| 状態確認         | `git status`                 |
| 履歴確認         | `git log`                    |
| 差分確認         | `git diff`                   |
| ファイル戻す     | `git restore ファイル名`     |
| ステージング     | `git add .`                  |
| 履歴に記録       | `git commit -m "メッセージ"` |
| GitHubに送信     | `git push`                   |

---

## 🧠 GitとGitHubの違い
- **Git**：ローカルで履歴を管理
- **GitHub**：クラウドで共有・保存・公開
- 使い分け：一人で使うならGitだけでもOK、チームや公開ならGitHubと連携

##🧠 補足：GitHubはいつ使うべき？
✔ バックアップをとりたいとき
✔ 他人と共有・チーム開発するとき
✔ ポートフォリオとして公開したいとき

---

##📌 重要ポイントまとめ
プロジェクトごとにディレクトリ＋Git初期化が基本
GitHub連携は必要なときだけでOK
1つのプロジェクトに対し1つのリポジトリが原則
Gitはローカル履歴管理、GitHubはクラウド共有ツール

Command+S（ファイルの保存）をしていなければ、git add → commit → push しても、その変更内容はGitにもGitHubにも反映されません。
- Gitはローカルで履歴管理
- GitHubはクラウドで共有・保存
- コマンドの順番：init → add → commit → push