## インストール

Neovim をインストールする。[参考](https://www.sambaiz.net/article/398/)

https://www.youtube.com/watch?v=stqUbv-5u2s

```sh
brew install neovim
which nvim

mkdir ~/.config/nvim
touch ~/.config/nvim/init.vim

brew tap daipeihust/tap && brew install im-select
```

`init.vim` を作成して、設定を追加する。

```
" ~/.config/nvim/init.vim
source ~/.vimrc
autocmd InsertLeave * :silent !/usr/local/bin/im-select com.apple.inputmethod.Kotoeri.RomajiTyping.Roman
```

`.vimrc` の設定をする。

```
" ~/.vimrc
" set clipboard+=unnamed
if exists('g:vscode')
    " VSCode extension
else
    " ordinary Neovim
endif
```

## nvim の設定

プラグインマネージャーをインストールする。

https://github.com/junegunn/vim-plug

```sh
mkdir ~/.config/nvim/plugged
```

`init.vim` にプラグインの設定を追加する。

```
" ~/.config/nvim/init.vim

...

" PLUGIN SETTINGS
call plug#begin('~/.config/nvim/plugged')

Plug '...'

call plug#end()
```

nvim を開いて下記コマンドを実行する。

```
:PlugInstall
```

nvim を再起動する。

## プラグインのインストール

### vim-surround

https://github.com/tpope/vim-surround

### fern

https://github.com/lambdalisue/fern.vim

```
:Fern .
:Fern . -drawer
```
