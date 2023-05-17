## インストール

注）[cargo](https://www.rust-lang.org/tools/install) のインストールを先におこなう必要がある。

https://www.lunarvim.org/docs/installation

```sh
LV_BRANCH='release-1.2/neovim-0.8' bash <(curl -s https://raw.githubusercontent.com/lunarvim/lunarvim/master/utils/installer/install.sh)
```

`.zshrc` に下記を追加する。

```
export PATH="$HOME/.local/bin/:$PATH"
```

### 設定

`~/.config/lvim/config.lua` を更新する。[参考](https://github.com/dhythm/config-public/blob/master/lvim/config.lua)

https://www.lunarvim.org/docs/configuration/language-features

```
lvim.lsp.installer.setup.automatic_installation = true

...

lvim.format_on_save.enabled = true
lvim.format_on_save = true

...

local formatters = require "lvim.lsp.null-ls.formatters"
formatters.setup {
  {
    command = "stylelint",
    filetypes = {
      "scss",
      "less",
      "css",
      "sass"
    },
    args = { "--fix", "--stdin" }
  },
  {
    command = "eslint_d",
    filetypes = {
      "javascriptreact",
      "javascript",
      "typescriptreact",
      "typescript",
    },
  },
  {
    command = "prettier",
    filetypes = {
      "javascript",
      "javascriptreact",
      "typescript",
      "typescriptreact",
      "css",
      "html",
      "json",
      "yaml",
      "markdown",
      "graphql"
    },
  },
  {
    command = "black",
    filetypes = {
      "python"
    }
  },
}

local linters = require "lvim.lsp.null-ls.linters"
linters.setup {
  {
    command = "eslint",
    filetypes = {
      "javascriptreact",
      "javascript",
      "typescriptreact",
      "typescript",
    },
  },
}

local code_actions = require "lvim.lsp.null-ls.code_actions"
code_actions.setup {
  {
    command = "eslint",
    args = { "-f" },
    filetypes = {
      "javascriptreact",
      "javascript",
      "typescriptreact",
      "typescript",
    },
  },
}

lvim.builtin.cmp.formatting.duplicates["nvim_lsp"] = 1
```
formatters/linters/code_actions に利用可能なものは[コチラ](https://github.com/jose-elias-alvarez/null-ls.nvim/blob/main/doc/BUILTINS.md#eslint-2)を参照。

formatters の設定で prettier を eslint_d より先に記載していた際に auto_fix が動作しないことがあった。


`eslint_d` をグローバルインストールする。

```sh
npm install -g eslint_d
```

code actions を実行する。

```
:lua vim.lsp.buf.code_action()
```

NerdFonts をインストールする。
https://www.lunarvim.org/docs/configuration/nerd-fonts

特定の拡張子のファイルを開こうとするとエラーが発生するので LSP をインストールする。

```
:Mason
:LspInstall prismals
:LspInstall jsonls
:LspInstall yamlls
```

### 起動

`:e <file_path>` でファイルを読み込む。ファイルのパスに移動する。

`:echo mapleader` で `<leader>` の表示ができる。
`<leader>e` でサイドバーを表示する。

タブとして表示されているものはバッファ機能が利用されている。
`<leader>bb` もしくは `:bnext` で次のバッファに移動可能。

バッファを確認する場合は `:ls`、消す場合は `:bw <number>` を実行する。

### 開発

- K: inspect
- gd: 定義にジャンプ
- gr: 参照にジャンプ

TypeScript をインストールする。

```
:TSInstall typescript
:TSInstall tsx
```

```
:LspInstall
```
