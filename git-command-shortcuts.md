# Git & GitHub コマンド ショートカット集

## ✅ プロジェクト初期化

```bash
mkdir my-project             # プロジェクト用ディレクトリ作成
cd my-project                # ディレクトリに移動
git init                     # Gitを初期化
```

## ✅ 初回コミットまでの基本操作

```bash
git add .                              # すべてのファイルをステージング（追加）
git commit -m "初回コミット"          # コメント付きでコミット
```

## ✅ GitHubとの連携（初回）

```bash
git remote add origin https://github.com/ユーザー名/リポジトリ名.git
git branch -M main                    # ブランチ名を main に統一（任意）
git push -u origin main               # GitHubへアップロード（初回のみ -u）
```

## ✅ 2回目以降の基本操作

```bash
git add .                              # 変更をステージに追加
git commit -m "変更内容の説明"        # コミット
git push                               # GitHubに反映
```

## ✅ 状況確認コマンド

```bash
git status         # 現在の変更状況を確認
git log            # コミット履歴を見る
git remote -v      # GitHubのリポジトリ連携状況を確認
```

## ✅ ブランチ操作（応用）

```bash
git branch                            # ブランチ一覧を確認
git checkout -b feature/new-idea      # 新しいブランチを作成して移動
git checkout main                     # mainブランチに戻る
git merge feature/new-idea           # 指定ブランチを現在のブランチにマージ
```

## ✅ よくあるエラーと対処法

| エラー内容 | 解決方法 |
|------------|----------|
| Nothing specified | git add . を忘れていないか確認 |
| unknown switch '-R' | git commit -m "コメント" を使う |
| remote origin already exists | git remote remove origin を実行 |
| Repository not found | GitHubのURLミス or 非公開設定確認 |

## ✅ Tips

- `git add .` は全変更をまとめてステージングしますが、特定のファイル名を指定してもOK
- `git commit -m "メッセージ"` のメッセージは必ず具体的に
- `git push` だけで GitHubに反映されるのは、一度 `-u` をつけて設定した後です 