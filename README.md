# GTK Demo

This is a GTK demo inside of a Python virtual environment.  It is known to work in Ubuntu 20.04.1 LTS.

## Environment Prep

### Install Pyenv

Update the apt cache

    sudo apt update -y

Install `pyenv` package dependencies

    sudo apt install -y make build-essential libssl-dev zlib1g-dev \
    libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm \
    libncursesw5-dev xz-utils tk-dev libffi-dev liblzma-dev python-openssl libncurses5-dev \
    git

Configure login scripts to load pyenv

    echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
    echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
    echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n eval "$(pyenv init -)"\nfi' >> ~/.bashrc

Reload the shell after install

    exec "$SHELL"

Test to make sure `pyenv` is in the path

    pyenv

### Install Python

Build it

    pyenv install 3.8.6

Activate it

    python global 3.8.6
    
Make sure the right version is active

    /usr/bin/env python --version

## GTK Demo

### Install Dependencies

    sudo apt install libcairo2-dev libgirepository1.0-dev
    pip install pycairo
    pip install PyGObject

### Run the demo

    ./run.py


