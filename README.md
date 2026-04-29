# Claude Code Routines — PR自動レビュー実践ガイド

Claude Code Routinesを使ったGitHub PR自動レビューの設定サンプル集です。

## デモページ

https://liatris000.github.io/liatris-20260429-claude-code-routines/

## 収録サンプル

| ファイル | 内容 |
|---------|------|
| `examples/pr-review.yml` | PRが開かれたとき自動レビュー |
| `examples/daily-report.yml` | 平日9時にデイリーレポートをSlackへ |
| `examples/ci-autofix.yml` | CI失敗時に自動修正コミット |

## 使い方

```bash
# サンプルをコピーして自分のリポジトリに配置
mkdir -p .claude/routines
cp examples/pr-review.yml .claude/routines/

# Claude Code CLIで登録
claude routines add .claude/routines/pr-review.yml

# 動作確認 (dry-run)
claude routines run pr-review --dry-run
```

## 注意

Claude Code Routinesは2026年4月現在リサーチプレビューです。仕様が変更される可能性があります。

- [公式ドキュメント](https://docs.anthropic.com/ja/docs/claude-code/routines)
- [Zenn記事](https://zenn.dev/liatris000)
