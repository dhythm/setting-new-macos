## Python のインストール

```sh
pyenv install --list
pyenv install <version>
pyenv versions

pyenv global <version>
pyenv local <version>
pyenv shell <version>
```

## Poetry

https://github.com/python-poetry/poetry

### Install

```sh
curl -sSL https://install.python-poetry.org | python3 -
echo '# poetry\nexport PATH="$HOME/.local/bin/:$PATH"' >> ~/.zshrc
```

### 利用方法

```sh
poetry new <project>
poetry install
poetry add <package>
poetry run python <program>
```
