# Volta

Node のバージョン管理ツール。
https://docs.volta.sh/guide/getting-started

## インストールと設定

```sh
curl https://get.volta.sh | bash

volta install node # install the latest LTS version
volta install node@22.5.1
```

```sh
npm login
```

`~/.npmrc` に設定を追加。

```
init.license=MIT
init.version=0.0.1
init.author.name=Yuta Okada
init.author.email=yuta.okada.20@gmail.com
init.author.url=https://github.com/dhythm
init.git.remote=https://github.com/dhythm/init.git
init.git.branch=main
init.git.ignore=node_modules
```
