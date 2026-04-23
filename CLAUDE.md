# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Git Rules

- After every code change, commit and push to GitHub immediately.
- Use clear, descriptive commit messages in English or Japanese.
- Always push to the remote branch that corresponds to the current local branch.
- Never force-push to `main` or `master` without explicit user confirmation.

```bash
git add <changed files>
git commit -m "description of change"
git push
```

## デプロイ先

https://kasa555302.github.io/task-board/

`main` ブランチへのプッシュで GitHub Actions が自動ビルド＆デプロイする（[.github/workflows/deploy.yml](.github/workflows/deploy.yml)）。

## 技術スタック

- **React 18** — UIフレームワーク
- **Vite 6** — ビルドツール・開発サーバー
- **CSS (plain)** — スタイリング（CSS-in-JSやUIライブラリは不使用）

主要コマンド：

```bash
npm run dev      # 開発サーバー起動 (http://localhost:5173)
npm run build    # プロダクションビルド → dist/
npm run preview  # ビルド結果をローカルでプレビュー
```

## コンポーネント命名規約

- ファイル名・コンポーネント名ともに **PascalCase**（例: `TaskItem.jsx`）
- 1ファイル1コンポーネントを原則とし、ファイル名とデフォルトエクスポート名を一致させる
- 対応するスタイルは同名の `.css` ファイルに記述（例: `App.jsx` → `App.css`）
