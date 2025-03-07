# Python

## インストール

```sh
pyenv install --list
pyenv install <version>
pyenv versions

pyenv global <version>
pyenv local <version>
pyenv shell <version>
```

## パッケージ管理ツール

### Poetry

https://github.com/python-poetry/poetry

#### インストール

```sh
curl -sSL https://install.python-poetry.org | python3 -
echo '# poetry\nexport PATH="$HOME/.local/bin/:$PATH"' >> ~/.zshrc
```

#### 使い方

```sh
poetry new <project>
poetry install
poetry add <package>
poetry run python <program>
```

### uv

https://github.com/astral-sh/uv
