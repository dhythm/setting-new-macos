# mise

ランタイムバージョン管理ツール。複数のプログラミング言語やツールのバージョンを統合管理できる。anyenv の後継として使える。

## インストール

[公式ページ](https://mise.jdx.dev/)にある方法でインストールする。

```sh
curl https://mise.run | sh
```

または Homebrew でインストールする。

```sh
brew install mise
```

## 設定

シェルの設定ファイル（`.zshrc` など）に以下を追加する。

```sh
eval "$(mise activate zsh)"
```

## 使い方

### ツールのインストール

```sh
mise install node@20
mise install python@3.12
mise install rust@1.75
```

### プロジェクトごとのバージョン指定

プロジェクトのルートに `.mise.toml` を作成する。

```toml
[tools]
node = "20.0.0"
python = "3.12.0"
```

### グローバルバージョンの設定

```sh
mise use --global node@20
mise use --global python@3.12
```
