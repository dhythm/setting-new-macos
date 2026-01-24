# Ghostty

クロスプラットフォームのターミナルエミュレータ。

## ダウンロード

https://ghostty.org/

## 設定

### 日本語対応フォントのインストール

```sh
brew install --cask font-jetbrains-mono
brew install --cask font-noto-sans-mono-cjk-jp
```

### 設定ファイルの編集

Ghostty の設定ファイル（`~/.config/ghostty/config`）を編集します。

```
# メイン（英数字・記号）
font-family = JetBrains Mono

# 日本語フォールバック（順番が大事）
font-family = Noto Sans Mono CJK JP
font-family = Noto Sans CJK JP

# サイズは好みで
font-size = 14

# 行間（日本語が詰まりやすい場合）
line-height = 1.2

# 太字をきれいに
font-thicken = true
```
