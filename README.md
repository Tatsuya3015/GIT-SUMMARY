# Git & GitHub 活用ガイド

このリポジトリでは、GitとGitHubの基本的な使い方と、ブランチ運用についてのガイドを提供しています。

## 📚 目次

1. [Git & GitHub の基本](#git--github-の基本)
2. [ブランチ運用ガイド](#ブランチ運用ガイド)

## Git & GitHub の基本

### 主な機能
- ローカルでの履歴管理（Git）
- クラウドでの共有・保存・公開（GitHub）

### 基本的な作業フロー
1. ファイルの編集
2. 保存（Command+S）
3. `git add`
4. `git commit`
5. `git push`

### よく使うコマンド
| 操作 | コマンド |
|------|----------|
| 状態確認 | `git status` |
| 履歴確認 | `git log` |
| 差分確認 | `git diff` |
| ファイル戻す | `git restore ファイル名` |
| ステージング | `git add .` |
| 履歴に記録 | `git commit -m "メッセージ"` |
| GitHubに送信 | `git push` |

## ブランチ運用ガイド

### ブランチとは
- 作業履歴の分岐（枝）
- 本線（main）とは別に、安全に実験や修正を行える作業スペース

### よくあるブランチの使い方
| ブランチ名 | 用途例 |
|------------|--------|
| `main` | 本番コード・安定した履歴 |
| `dev` | 開発中コード |
| `feature/xxx` | 機能追加用 |
| `bugfix/xxx` | バグ修正用 |
| `hotfix/xxx` | 緊急パッチ用 |

### ブランチの基本操作
```bash
# ブランチ一覧表示
git branch

# 新しいブランチ作成と移動
git checkout -b ブランチ名

# ブランチの切り替え
git checkout ブランチ名
```

### ブランチ運用のベストプラクティス
- mainブランチへの直接pushは避ける
- 機能追加はfeatureブランチで行う
- コミットは小さく、意味のある単位で行う
- Pull Requestを活用してコードレビューを行う

## 詳細なガイド
- [Git & GitHub 活用の基本ステップ](./git-github-summary.md)
- [Gitブランチ完全ガイド](./git-branch-guide.md) 