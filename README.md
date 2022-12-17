# MacBook Pro セットアップ

## 設定

### `System Settings > Accessibility`

- `Trackpad Options... > Scroll speed` を Fast に設定

### `System Settings > Trackpad`

- `Tracking speed` を Fast に設定
- `Tap to click` を ON に設定
- `Look up & data detectors` を `Tap with Three Fingers` に変更

### `System Settings > Keyboard`

- `Key repeat rate` を Fast に設定
- `Delay until repeat` を Short に設定
- `Touch Bar Settings... > Touch Bar shows` を `F1, F2, etc. Keys` に変更
- `Keyboard Shortcuts... > Modifier Keys` で `Caps Lock key` を `Control` に変更
- `Keyboard Shortcuts... > Input Sources` で `Select next source in Input menu` を `Cmd + Space` に変更
- `Keyboard Shortcuts... > Spotlight` で `Show Spotlight search` を無効化

### `System Settings > Desktop & Dock`

- `Size` を調整
- `Automatically hide and show the Dock` を ON に設定
- Dock から不要なアプリケーションを削除

### `System Settings > Screen Saver`

- `Hello` に変更

### `System Settings > Control Center`

- `Bluetooth` を表示
- `Sound` を `Always Show in Menu Bar` に設定
- `Battery > Show Percentage` を ON に設定

### `System Settings > Displays`

- `More Space` を選択

### `System Settings > General`

- `About > name` で変更

### `System Settings > Privacy & Security`

- `FileVault` が Turn On であることを確認（デフォルト設定）

### `Finder > Settings`

- `Sidebar` の設定を変更
- `Advanced > Show all filename extensions` を選択
- `View > as Columns` を選択
- `View > Show Tab Bar` を選択
- `View > Show Path Bar` を選択

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

- AutoPagerize
- DeepL Translate
- Douga Getter
- EyeDropper
- Google Translate
- Grammarly
- Keepa
- LastPass
- Lighthouse
- React Developer Tools
- Video Speed Controller
- Vimium
- Wappalyzer
- WhatFont

### Raycast

- `General > Reycast Hotkey` を `Ctrl + Space` に変更

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

### Docker Desktop for Mac

本体のリソースを消費しすぎないよう、`Preferences > Resources` をチェックする。

- CPUs: 4
- Memory: 8 GB
- Swap: 1 GB

### Fonts

### Git

### Homebrew

[公式ページ](https://brew.sh/)にあるコマンドを実行する。
Xcode Command Line Tools がない場合はインストールされる。

インストール後、手動でパスを設定する。

```sh
echo '# Set PATH, MANPATH, etc., for Homebrew.' >> /Users/USERNAME/.zprofile
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/USERNAME/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

### MacVim

[GitHub](https://github.com/macvim-dev/macvim)のページからダウンロードする。
以下の設定ファイルを更新する。

- `/Applications/MacVim.app/Contents/Resources/vim/vimrc`
- `/Applications/MacVim.app/Contents/Resources/vim/gvimrc`

それぞれの設定ファイルは下記の通り。

- https://github.com/dhythm/config-public/blob/master/.vimrc
- https://github.com/dhythm/config-public/blob/master/.gvimrc

### VS Code

コマンドパレットを起動（`Cmd+Shift+P`）し、`Shell Command: Install 'code' command PATH` を実行する。

拡張をインストールする。[参考](https://github.com/dhythm/config-public/blob/master/vscode-extensions.txt)

VSCodeVim の設定をする。[参考](https://marketplace.visualstudio.com/items?itemName=vscodevim.vim)

```sh
$ defaults write com.microsoft.VSCode ApplePressAndHoldEnabled -bool false              # For VS Code
$ defaults write com.microsoft.VSCodeInsiders ApplePressAndHoldEnabled -bool false      # For VS Code Insider
$ defaults write com.visualstudio.code.oss ApplePressAndHoldEnabled -bool false         # For VS Codium
$ defaults write com.microsoft.VSCodeExploration ApplePressAndHoldEnabled -bool false   # For VS Codium Exploration users
$ defaults delete -g ApplePressAndHoldEnabled
```

### anyenv

### ffmpeg

Homebrew を使ってイントールする。

```sh
brew install ffmpeg
```

### Oh My Zsh

[公式ページ](https://ohmyz.sh/#install)に従い、インストールする。

完了後、[powerlevel10k](https://github.com/romkatv/powerlevel10k) をインストールする。

### iTerm2

- `Preferences > Profiles > Text` の `Cursor` を Underline に変更
- `Preferences > Profiles > Text` の `Blinking cursor` を ON に変更
- `Preferences > Profiles > Session` の `Automatically log session input to files in:` にチェックをつけてログを取得

### volta

### Others

- [ ] Android Studio
- [ ] Figma
- [ ] Tandem
- [ ] TablePlus
- [ ] Xcode
