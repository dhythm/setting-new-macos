## インストール

https://www.lunarvim.org/docs/installation

```sh
LV_BRANCH='release-1.2/neovim-0.8' bash <(curl -s https://raw.githubusercontent.com/lunarvim/lunarvim/master/utils/installer/install.sh)
```

`.zshrc` に下記を追加する。
```
export PATH="$HOME/.local/bin/:$PATH"
```

### 設定

`~/.config/lvim/config.lua` を更新する。

```
lvim.format_on_save.enabled = true
lvim.format_on_save = true
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

