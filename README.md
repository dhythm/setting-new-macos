# MacBook Pro セットアップ

## 設定

### `System Settings > Keyboard`

- `Key repeat rate` を Fast に設定
- `Delay until repeat` を Short に設定
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

### `Applications > Utilities > Terminal.app`

下記のコマンドを実行して PC を再起動。

```
defaults write -g ApplePressAndHoldEnabled -bool false
```

## アプリケーション

### ブラウザ

#### [Google Chrome](docs/google-chrome.md)

#### [Sidekick](docs/sidekick.md)

### 業務効率化

#### [Raycast](docs/raycast.md)

#### [ChatGPT](docs/chat-gpt.md)

### ターミナル

#### [iTerm2](docs/iterm2.md)

#### [Oh My Zsh](docs/oh-my-zsh.md)

#### [Homebrew](docs/homebrew.md)

#### [Git / GitHub](docs/git-and-github.md)

#### [anyenv](docs/anyenv.md)

#### [volta](docs/volta.md)

### エディタ

#### [Visual Studio Code](docs/vscode.md)

#### [Cursor](./docs/cursor.md)

#### [NeoVim](docs/nvim.md)

#### [LunarVim](docs/lunar-vim.md)

#### [MacVim](docs/macvim.md)

### その他

- [Bear](https://bear.app/)
- [DeepL](https://www.deepl.com/en/macos-app/)
- [Discord](https://discord.com/download)
- [Gapplin](https://apps.apple.com/jp/app/gapplin/id768053424?mt=12)
- [LINE](https://apps.apple.com/jp/app/line/id539883307?mt=12)
- [Slack](https://slack.com/downloads/mac)
- [Zoom](https://zoom.us/download)



### Docker Desktop for Mac

本体のリソースを消費しすぎないよう、`Preferences > Resources` をチェックする。

- CPUs: 4
- Memory: 8 GB
- Swap: 1 GB

![](./assets/img/docker.png)

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
