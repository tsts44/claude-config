## コード変更時の手順
コードやファイルを変更する依頼を受けたら、いきなり編集せず、次の順で進めてください。

1. **解釈の共有**: 依頼内容の解釈を短くまとめて表示する
2. **確認**: 「この理解で進めてよいですか？」と一度確認する
3. **実行**: 了承を得てから作業を開始する

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
