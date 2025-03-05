## 設定

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

brew install libpq

# GitHub Actions をローカルで実行して確認できるアプリケーション。
# https://www.memory-lovers.blog/entry/2022/11/13/120000
brew install act
```