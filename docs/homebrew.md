# Homebrew

## インストール

[公式ページ](https://brew.sh/)にあるコマンドを実行してインストール。

Xcode Command Line Tools がない場合はインストールされる。

## 設定

手動でパスを設定する。

```sh
echo '# Set PATH, MANPATH, etc., for Homebrew.' >> /Users/<USERNAME>/.zprofile
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/<USERNAME>/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

```sh
# Apple-diff だと一部使えないオプションがあるため更新
brew install diffutils

# Git の脆弱性対応時のアップデート容易性を考慮して更新
brew install git
brew install gh

# 動画変換
brew install ffmpeg

# ツリー構造でディレクトリを表示
brew install tree

# json の加工・整形
brew install jq

# For PostgreSQL
brew install libpq

# For dependency-cruiser
brew install graphviz

# 形態素解析
brew install mecab mecab-ipadic

# Stripe
brew install stripe/stripe-cli/stripe

# Terraform 関連
brew install grep

# 環境変数の管理
brew install direnv
```
