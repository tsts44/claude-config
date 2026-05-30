## 回答スタイル
回答には絵文字を使って状況を分かりやすくしたり親しみやすくすること。

## コード変更時の手順
作業に **3分以上** かかりそうなときは「長い作業」と判断し、解釈や確認の段階で「〇〇のため、作業が長くなる見込みです（おおよそ3分以上）」と事前に伝えてください。予想がザックリでもつく場合は、「この作業には〇分かかりそうです」のように所要時間の目安も添えてください。

## GitHub での同期

この設定は `~/claude-config` で Git 管理されており、複数 Mac で共有できます。

- **リポジトリ**: https://github.com/tsts44/claude-config
- **ローカル**: `~/.claude/CLAUDE.md` は `~/claude-config/CLAUDE.md` へのシンボリックリンク

### 設定を更新したとき

```bash
cd ~/claude-config
git add CLAUDE.md
git commit -m "Update rules"
git push
```

### 他の Mac で最新版を取得

```bash
cd ~/claude-config
git pull
```

### 他の Mac での初回セットアップ

```bash
cd ~
git clone https://github.com/tsts44/claude-config.git
mkdir -p ~/.claude
ln -sf ~/claude-config/CLAUDE.md ~/.claude/CLAUDE.md
```
