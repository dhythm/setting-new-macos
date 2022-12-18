# MacBook Pro セットアップ

## 設定

### `System Settings > General`

- `About > name` で変更


### `System Settings > Accessibility`

- `Pointer Control > Trackpad Options... > Scroll speed` を Fast に設定

![](./assets/img/scroll_speed.png)

### `System Settings > Control Center`

- `Bluetooth` を表示
- `Sound` を `Always Show in Menu Bar` に設定
- `Battery > Show Percentage` を ON に設定


![](./assets/img/control_center_01.png)
![](./assets/img/control_center_02.png)

### `System Settings > Desktop & Dock`

- `Size` を調整
- `Automatically hide and show the Dock` を ON に設定
- Dock から不要なアプリケーションを削除

### `System Settings > Displays`

- `More Space` を選択

![](./assets/img/display.png)

### `System Settings > Screen Saver`

- `Hello` に変更


### `System Settings > Keyboard`

- `Key repeat rate` を Fast に設定
- `Delay until repeat` を Short に設定
- `Touch Bar Settings... > Touch Bar shows` を `F1, F2, etc. Keys` に変更
- `Keyboard Shortcuts... > Input Sources` で `Select the previous source in Input menu` を `Cmd + Space` に変更
- `Keyboard Shortcuts... > Input Sources` で `Select next source in Input menu` を `Cmd + Shift + Space` に変更
- `Keyboard Shortcuts... > Spotlight` で `Show Spotlight search` を無効化
- `Keyboard Shortcuts... > Modifier Keys` で `Caps Lock key` を `Control` に変更

![](./assets/img/keyboard_01.png)
![](./assets/img/keyboard_02.png)
![](./assets/img/keyboard_03.png)
![](./assets/img/keyboard_04.png)
![](./assets/img/keyboard_05.png)

### `System Settings > Trackpad`

- `Tracking speed` を Fast に設定
- `Look up & data detectors` を `Tap with Three Fingers` に変更
- `Tap to click` を ON に設定

![](./assets/img/trackpad.png)

### `System Settings > Privacy & Security`

- `FileVault` が Turn On であることを確認（デフォルト設定）

### `Finder > Settings`

- `Sidebar` の設定を変更
- `Advanced > Show all filename extensions` を選択
- `View > as Columns` を選択
- `View > Show Tab Bar` を選択
- `View > Show Path Bar` を選択

![](./assets/img/finder_01.png)
![](./assets/img/finder_02.png)

## アプリケーション（一般）

### Google Chrome

### Sidekick

##### Settings

- Google account でログインすることで設定を共有

##### Bookmarks

- 2022/12 時点では同期されない
- 旧 PC の Bookmark Manager から export
- 新 PC で `Bookmarks > Import Bookmarks and Settings...` にて import

##### Passwords

- 2022/12 時点では同期されない
- `Settings > Autofill > Password Manager > Saved Passwords` から `Export passwords...` を実行
- `chrome://flags/` で `Password import` を Enabled に変更（要：再起動）
- `Settings > Autofill > Password Manager > Saved Passwords` から `Import passwords...` を実行

##### Extensions

- [ ] AutoPagerize
- [ ] DeepL Translate
- [ ] Douga Getter
- [ ] EyeDropper
- [ ] Google Translate
- [ ] Grammarly
- [ ] Keepa
- [ ] LastPass
- [ ] Lighthouse
- [ ] React Developer Tools
- [ ] Video Speed Controller
- [ ] Vimium
- [ ] Wappalyzer
- [ ] WhatFont

### Raycast

- `General > Reycast Hotkey` を `Ctrl + Space` に変更

![](./assets/img/raycast.png)

### Others

- [ ] Bear
- [ ] DeepL
- [ ] Discord
- [ ] Gapplin
- [ ] LINE
- [ ] Slack
- [ ] Spectacle
- [ ] Zoom

## アプリケーション（開発）

### iTerm2

- `Preferences > Profiles > Text` の `Cursor` を Underline に変更
- `Preferences > Profiles > Text` の `Blinking cursor` を ON に変更
- `Preferences > Profiles > Session` の `Automatically log session input to files in:` にチェックをつけてログを取得

![](./assets/img/iterm2.png)

### Oh My Zsh

[公式ページ](https://ohmyz.sh/#install)に従い、インストール。
完了後、[powerlevel10k](https://github.com/romkatv/powerlevel10k) をインストールする。

`.zshrc` を設定する。[参考](https://github.com/dhythm/config-public/blob/master/.zshrc)

### Homebrew

[公式ページ](https://brew.sh/)にあるコマンドを実行する。
Xcode Command Line Tools がない場合はインストールされる。
インストール後、手動でパスを設定する。

```sh
echo '# Set PATH, MANPATH, etc., for Homebrew.' >> /Users/USERNAME/.zprofile
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/USERNAME/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

### Git / GitHub

`git` は初期からインストールされているので `.gitconfig` の設定をする。[参考](https://github.com/dhythm/config-public/blob/master/.gitconfig)

次に GitHub を利用する設定をする。
```sh
ssh-keygen -t ed25519 -C "your_email@example.com"
eval "$(ssh-agent -s)"

touch ~/.ssh/config
```

`~/.ssh/config` を設定する。
```
Host *.github.com
  AddKeysToAgent yes
  UseKeychain yes
  IdentityFile ~/.ssh/id_ed25519
```

公開鍵をクリップボードに取得する。
```sh
ssh-add --apple-use-keychain ~/.ssh/id_ed25519
pbcopy < ~/.ssh/id_ed25519.pub
```

GitHub のウェブページにアクセスし、`Settings > SSH and GPG keys` を選択。
SSH keys に取得した公開鍵を貼り付けて保存する。

### Docker Desktop for Mac

本体のリソースを消費しすぎないよう、`Preferences > Resources` をチェックする。

- CPUs: 4
- Memory: 8 GB
- Swap: 1 GB

![](./assets/img/docker.png)


### MacVim

[GitHub](https://github.com/macvim-dev/macvim)のページからダウンロードする。
以下の設定ファイルを更新する。

- `/Applications/MacVim.app/Contents/Resources/vim/vimrc`
- `/Applications/MacVim.app/Contents/Resources/vim/gvimrc`

それぞれの設定ファイルは下記の通り。

- https://github.com/dhythm/config-public/blob/master/.vimrc
- https://github.com/dhythm/config-public/blob/master/.gvimrc

### VS Code

##### code コマンドの有効化

コマンドパレットを起動（`Cmd+Shift+P`）し、`Shell Command: Install 'code' command PATH` を実行する。

##### setting.json

setting.json を設定する。[参考](https://github.com/dhythm/config-public/blob/master/vscode-settings.json)

- `vscode-neovim.neovimExecutablePaths.darwin` に `which nvim` で取得したパスを設定する
- `terminal.integrated.fontFamily` にターミナルで設定しているフォントを指定する
- Operator Mono Lig フォントをインストール（[参考](https://github.com/kiliman/operator-mono-lig)）

##### Extensions

拡張をインストールする。[参考](https://github.com/dhythm/config-public/blob/master/vscode-extensions.txt)

##### Keybindings

`keybindings.json` を更新する。[参考](https://github.com/dhythm/config-public/blob/master/keybindings.nvim.json)

Neovim をインストールする。[参考](https://www.sambaiz.net/article/398/)

init.vim を作成して、設定を追加する。

```sh
brew install neovim
which neovim

mkdir ~/.config/nvim
touch ~/.config/nvim/init.vim

brew tap daipeihust/tap && brew install im-select
vi ~/.config/nvim/init.vim
```

```
source ~/.vimrc
autocmd InsertLeave * :silent !/usr/local/bin/im-select com.apple.inputmethod.Kotoeri.RomajiTyping.Roman
```

TODO: ~/.vimrc の設定をする。

### anyenv

https://github.com/anyenv/anyenv

```sh
brew install anyenv
anyenv init
anyenv install --init
git clone https://github.com/anyenv/anyenv ~/.anyenv

anyenv install pyenv
```

node のバージョンは volta にて管理するため、nodenv はインストールしない。

### volta

https://docs.volta.sh/guide/getting-started
```sh
curl https://get.volta.sh | bash

volta install node@16.12.0

npm login
```


### ffmpeg

Homebrew を使ってイントールする。

```sh
brew install ffmpeg
```

### Others

- [ ] Android Studio
- [ ] Figma
- [ ] Tandem
- [ ] TablePlus
- [ ] Xcode
