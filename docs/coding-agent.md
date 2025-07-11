# Coding Agent

## Claude Code

1. インストール

```sh
npm install -g @anthropic-ai/claude-code

claude
claude --dangerously-skip-permissions
```

2. MCP サーバーのインストール

```sh
# グローバルインストール（永続的）: ~/.claude.json に保存される
claude mcp add playwright -s user npx @playwright/mcp@latest

# グローバルインストール（セッション）
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
gemini --yolo

npx https://github.com/google-gemini/gemini-cli
```

2. コマンドライン実行

```sh
gemini -p "検索内容"
```

## Codex CLI

```sh
npm install -g @openai/codex
```
