
## インストール

[公式ページ](https://github.com/anyenv/anyenv)にある方法でインストールする。

```sh
brew install anyenv
```

## 設定

```sh
anyenv init
anyenv install --init
anyenv install pyenv
anyenv install rbenv
```

### Node.js

node のバージョンは volta にて管理するため、nodenv はインストールしない。

### [Python](./python.md)