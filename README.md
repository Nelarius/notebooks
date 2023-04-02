# Tl;DR argh I just want to activate my python env

```sh
# Here's how I created this environment:
$ pyenv virtualenv 3.11.1 notebooks
$ pyenv local notebooks
$ pyenv which python
```
The environment will be activated if you add the following snippet to your `.zshrc`:

## Add the following to `.zshrc`

```sh
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"
```

```sh
# This is the command I would have to run manually otherwise
$ pyenv activate notebooks
```

# Pyenv-virtualenv setup

Following [this](https://realpython.com/intro-to-pyenv/) tutorial.

## Listing Python versions

```sh
$ pyenv install --list | rg " 3\.[678910]"
```

## Installing Python

```sh
$ pyenv install -v 3.11.1
```

## Seeing installed versions

```sh
$ pyenv versions
# Python versions are in the pyenv root directory
$ ls ~/.pyenv/versions
```

## Setting the global python version

```sh
$ pyenv global 3.11.1
```

## Setting local python version

```sh
# Creates a .python-version file in your current directory
$ pyenv local 3.11.1
```

## Setting shell-specific python version

```sh
# Sets the PYENV_VERSION environment variable
$ pyenv shell 3.11.1
```