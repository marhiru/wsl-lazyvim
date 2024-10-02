# Welcome to my Linux terminal setup and config

## First we need to install HomeBrew for linux 

### Linux Brew setup

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### Now add Linux Brew to terminal PATH

```bash
test -d ~/.linuxbrew && eval "$(~/.linuxbrew/bin/brew shellenv)"
test -d /home/linuxbrew/.linuxbrew && eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"
echo "eval \"\$($(brew --prefix)/bin/brew shellenv)\"" >> ~/.bashrc
```

### To finish Linux Brew SETUP install this required dependencies

```bash
sudo apt-get install build-essentials && sudo apt update
```

### First dependency install on Linux Brew

```bash
brew install gcc
```

## Now we go to start our neo/lazy vim setup

### Install neovim

```bash
brew install neovim
```

## Ok, before installing LazyVim, we need to setup our cli superpowers (oh-my-fish) Fish Shell + oh-my-zsh

First, we install Fish Shell

```bash
brew install fish
```

Second, we need to install the oh-my-fish with curl method like on official repository

```bash
curl https://raw.githubusercontent.com/oh-my-fish/oh-my-fish/master/bin/install | fish
```

## And to finish oh-my-fish setup we need to set this shell on default settings

First you need to reach bashrc file
```bash
sudo vim ~/.bashrc
```

Add this to final line in bashrc

```bash
fish
```

## Finally we now can start to setup our WorkFlow Structure using LazyVim

### First we need to setup our Lazy vim imports file structure

Adding nvim to ~/.config/ files

```bash
mkdir ~/.config/nvim
```

Creating init.lua inside nvim folder (use this cli inside ~/.config/nvim folder)

```bash
vim init.lua
```

Create a whole file structure (assuming your inside of ~/.config/nvim)

PATH ~/.config/nvim/lua

```bash
mkdir lua
```

PATH ~/.config/nvim/lua/config

```bash
mkdir lua/config
```

## Now your terminal and Lazyvim are ready!
