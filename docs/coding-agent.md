# Coding Agent

## Claude Code

1. インストール

```sh
npm install -g @anthropic-ai/claude-code
claude
```

2. MCP サーバーのインストール

```sh
# グローバルインストール
claude mcp add playwright npx @playwright/mcp@latest

# ローカルインストール
 claude mcp add -s project playwright npx @playwright/mcp@latest
```

3. カスタムコマンドの作成

```sh
# グローバルインストール
mkdir ~/.claude/commands
touch ~/.claude/commands/gemini-search.md

# ローカルインストール
mkdir .claude/commands
touch .claude/commands/gemini-search.md
```

## gemini-cli

1. インストール

```sh
npm install -g @google/gemini-cli
gemini # 初期化フロー
```

2. コマンドライン実行

```sh
gemini -p "検索内容"
```

## Codex CLI

```sh
npm install -g @openai/codex
```
