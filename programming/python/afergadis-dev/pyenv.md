# pyenv
[`pyenv`](https://github.com/pyenv/pyenv) is a simple Python version manager.
Except the official documentation, a nice guide is [here](
https://realpython.com/intro-to-pyenv/)

## Build Dependencies
We need some packages for `pyenv` to build the Python versions. Run the
following command:
```bash
sudo apt-get install -y make build-essential libssl-dev zlib1g-dev \
libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev \
libncursesw5-dev xz-utils tk-dev libffi-dev liblzma-dev python-openssl
```
## Installation
Install `pyenv`:
```bash
curl https://pyenv.run | bash
```

Open the `~/.bashrc` file and append the following:
```
# Load pyenv automatically 

export PYENV_ROOT="$HOME/.pyenv"
command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"
eval "$(pyenv init -)"

# Load pyenv-virtualenv automatically 

eval "$(pyenv virtualenv-init -)"
```

 Restart your shell for the changes to take effect.
```bash
exec $SHELL
```
