# MacBook Pro セットアップ

## 設定

### `System Settings > General`

- `About > name` で変更

### `System Settings > Accessibility`

- `Pointer Control > Trackpad Options... > Scroll speed` を Fast に設定

![](./assets/img/scroll_speed.png)

### `System Settings > Accessibility`

- 検索欄で `camera` と入力すると `Camera Options...` が表示される
- `Camera Options...` から内蔵カメラ/外付けカメラの切り替えができる

![](./assets/img/camera_options.png)

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

### `System Settings > Touch ID & Password`

- Apple Watch で Mac のアンロックを有効にする

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

### その他

- [Bear](https://bear.app/)
- [DeepL](https://www.deepl.com/en/macos-app/)
- [Discord](https://discord.com/download)
- [Gapplin](https://apps.apple.com/jp/app/gapplin/id768053424?mt=12)
- [LINE](https://apps.apple.com/jp/app/line/id539883307?mt=12)
- [Slack](https://slack.com/downloads/mac)
- [Spectacle](https://www.spectacleapp.com/)
- [Zoom](https://zoom.us/download)

## 開発環境

### iTerm2

- `Preferences > Profiles > Text` の `Cursor` を Underline に変更
- `Preferences > Profiles > Text` の `Blinking cursor` を ON に変更
- `Preferences > Profiles > Window` の `Transparency` を変更（Oh My Zsh の設定で透過対応が必要）
- `Preferences > Profiles > Session` の `Automatically log session input to files in:` にチェックをつけてログを取得

![](./assets/img/iterm2.png)

### Oh My Zsh

https://ohmyz.sh/#install

注）XCode のインストールを先に実施する必要がある。

[powerlevel10k](https://github.com/romkatv/powerlevel10k) をインストール。

`.zshrc` を[設定](https://github.com/dhythm/config-public/blob/master/.zshrc)。

### Homebrew

https://brew.sh/

Xcode Command Line Tools がない場合はインストールされる。
インストール後、手動でパスを設定する。

```sh
echo '# Set PATH, MANPATH, etc., for Homebrew.' >> /Users/USERNAME/.zprofile
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/USERNAME/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

```sh
# Apple-diff だと一部使えないオプションがあるため更新
brew install diffutils

# Git の脆弱性対応時のアップデート容易性を考慮して更新
brew install git

brew install ffmpeg

brew install tree

brew install jq

# GitHub Actions をローカルで実行して確認できるアプリケーション。
# https://www.memory-lovers.blog/entry/2022/11/13/120000
brew install act
```

### Git / GitHub

`.gitconfig` の[設定](https://github.com/dhythm/config-public/blob/master/.gitconfig)。

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

### エディタ

#### MacVim

https://github.com/macvim-dev/macvim

以下の設定ファイルを更新する。

- `/Applications/MacVim.app/Contents/Resources/vim/vimrc`
- `/Applications/MacVim.app/Contents/Resources/vim/gvimrc`

それぞれの設定ファイルは下記の通り。

- [vimrc](https://github.com/dhythm/config-public/blob/master/macvim/vimrc)
- [gvimrc](https://github.com/dhythm/config-public/blob/master/macvim/gvimrc)

#### NeoVim

[設定](docs/nvim.md)

#### LunarVim

[設定](docs/lunar-vim.md)

#### VS Code

[設定](docs/vscode.md)

### バージョン管理 / プログラミング言語

#### anyenv

https://github.com/anyenv/anyenv

```sh
brew install anyenv
anyenv init
anyenv install --init
git clone https://github.com/anyenv/anyenv ~/.anyenv

anyenv install pyenv
anyenv install rbenv
```

node のバージョンは volta にて管理するため、nodenv はインストールしない。

[python の設定](docs/python.md)

#### volta

https://docs.volta.sh/guide/getting-started

```sh
curl https://get.volta.sh | bash

volta install node@16.12.0

npm login
```

`.npmrc` に設定を追加。

```
init.license=MTI
init-version=0.0.1
```

#### Deno

https://deno.land/manual@v1.29.2/getting_started/installation

```sh
curl -fsSL https://deno.land/x/install/install.sh | sh
```

`.zshrc` にパスを追加する。

```
export PATH="$HOME/.deno/bin:$PATH"
```

#### CocoaPods

```sh
sudo gem install cocoapods
```

#### Rust

https://www.rust-lang.org/tools/install

```sh
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

### その他

#### Slack for Developer

https://api.slack.com/future/quickstart

```sh
curl -fsSL https://downloads.slack-edge.com/slack-cli/install.sh | bash
```

表示されるスラッシュコマンドを Slack で実行。

```sh
/slackauthticket xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

Slack アプリケーションを作成。

```sh
slack create <app_name>
```

#### アプリケーション

- [Android Studio](https://developer.android.com/studio?gclsrc=ds&gclsrc=ds)
- [Figma](https://www.figma.com/downloads/)
- [Tandem](https://tandem.chat/welcome/download)
- [TablePlus](https://tableplus.com/download)
- [Xcode](https://apps.apple.com/us/app/xcode/id497799835?mt=12)
