# Git / GitHub

## 設定

下記のコマンドで設定を追加できる。

```sh
git config --global user.name 'dhythm'
git config --global user.email 'yuta.okada.20@gmail.com'
```

`~/.gitconfig` を開き、[設定](https://github.com/dhythm/config-public/blob/master/.gitconfig)を反映。

### GitHub configuration

```sh
ssh-keygen -t ed25519 -C "your_email@example.com"
eval "$(ssh-agent -s)"

touch ~/.ssh/config
```

`~/.ssh/config` 開く。

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

GitHub のウェブページにアクセスし、`Settings > SSH and GPG keys > New SSH Key` を選択。
Title を設定（推奨は PC の名称等）し、Key type に `Authentication Key`、Key にコピーした公開鍵を貼り付けて保存する。
