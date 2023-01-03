
## nvim のインストール

Neovim をインストールする。[参考](https://www.sambaiz.net/article/398/)

https://www.youtube.com/watch?v=stqUbv-5u2s

```sh
brew install neovim
which neovim

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
set clipboard+=unnamed
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

Plug 'tpope/vim-surround'

call plug#end()
```

