# Claude グローバル設定

Claude Code のグローバル `CLAUDE.md` を Git で管理するリポジトリです。
複数の Mac で同じ設定を共有できます。

## 初回セットアップ（この Mac）

```bash
# 1. リポジトリをクローン（または既にクローン済みの場合）
cd ~
git clone <このリポジトリのURL> claude-config
cd claude-config

# 2. ~/.claude にシンボリックリンクを作成
mkdir -p ~/.claude
ln -sf ~/claude-config/CLAUDE.md ~/.claude/CLAUDE.md
```

## 他の Mac でのセットアップ

```bash
# 1. リポジトリをクローン
cd ~
git clone <このリポジトリのURL> claude-config
cd claude-config

# 2. ~/.claude にシンボリックリンクを作成
mkdir -p ~/.claude
ln -sf ~/claude-config/CLAUDE.md ~/.claude/CLAUDE.md
```

## 設定の更新

```bash
cd ~/claude-config
# CLAUDE.md を編集後
git add CLAUDE.md
git commit -m "Update CLAUDE.md"
git push
```

## 他の Mac で最新版を取得

```bash
cd ~/claude-config
git pull
```

## ファイル構成

```
claude-config/
├── CLAUDE.md   # グローバル設定（~/.claude/CLAUDE.md にリンク）
└── README.md   # このファイル
```
