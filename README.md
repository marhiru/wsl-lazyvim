# Welcome to my Linux terminal setup and config

## First of all we need to install HomeBrew for linux (LinuxBrew)

Linux Brew **SETUP**

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Adding LinuxBrew to terminal **PATH**

```bash
test -d ~/.linuxbrew && eval "$(~/.linuxbrew/bin/brew shellenv)"
test -d /home/linuxbrew/.linuxbrew && eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"
echo "eval \"\$($(brew --prefix)/bin/brew shellenv)\"" >> ~/.bashrc
```

Required dependencies To finish LinuxBrew **SETUP** 

```bash
sudo apt-get install build-essentials && brew install gcc
```
**Update to check if everything is ok**
```bash
sudo apt update
```

Testing if LinuxBrew are installed

```bash
brew  --version
```

## Setup terminal plugin (oh-my-fish) Fish Shell + oh-my-zsh

First, we install Fish Shell

```bash
brew install fish
```

Second, we need to install the oh-my-fish with curl method like on official repository

```bash
curl https://raw.githubusercontent.com/oh-my-fish/oh-my-fish/master/bin/install | fish
```

And to finish oh-my-fish setup we need to set this shell on default settings

First you need to reach bashrc file
```bash
sudo vim ~/.bashrc
```

Add this to final line in bashrc

```bash
fish
```

# Lets setup lazyvim 

Install neovim (If already installed, skip this step)

```bash
brew install neovim
```

### Creating nvim folder in **PATH**  ```~/.config```

```bash
 cd ~/.config && mkdir nvim
```
or
```bash
mkdir ~/.config/nvim
```

_________________________________________________________

### Creating lua folder in **PATH**  ```~/.config/nvim```

```bash
cd nvim && mkdir lua
```
or
```bash
mkdir ~/.config/nvim/lua
```

______________________________________________________________

### Creating config folder in **PATH** ```~/.config/nvim/lua```

```bash
cd lua && mkdir config
```
or
```bash
mkdir ~/.config/nvim/lua/config
```


## Initializing Lazyvim

**Create init file**

```bash
cd ~/.config/nvim && vim init.lua
```

[init.lua content](https://github.com/marhiru/vim-setup/blob/main/init.lua)

## Configure Lazyvim
### Now we ahead to setup your own config, have mine for example but dont bindly copy & paste, use as inpiration and have your own

**Creating keymaps presets file**

```bash
cd ~/.config/nvim/lua/config && vim keymaps.lua
```

[keymaps.lua content](https://github.com/marhiru/vim-setup/blob/main/keymaps.lua)

_________________________________________________________________________________

**Creating autocmds presets file**

```bash
cd ~/.config/nvim/lua/config && vim autocmds.lua
```

[autocmds.lua content](https://github.com/marhiru/vim-setup/blob/main/autocmds.lua)

___________________________________________________________________________________

**Creating lazyvim setup file**

```bash
cd ~/.config/nvim/lua/config && vim lazy.lua
```

[lazy.lua content](https://github.com/marhiru/vim-setup/blob/main/lazy.lua)

___________________________________________________________________________

**Creating opts (options) config file**

```bash
cd ~/.config/nvim/lua/config && vim options.lua
```

[options.lua content](https://github.com/marhiru/vim-setup/blob/main/options.lua)

________________________________________________________________________________

### Now create a folder with whatever name you want on PATH ```~/.config/nvim/lua```
**This folder will contain discipline.lua and theme config files**

I will create the folder with the same of my user **zero**

```bash
  mkdir zero
```

Go on the folder

```bash
cd zero
```

### We gonna finals setup ```discipline.lua``` / ```hsl.lua``` / ```lsp.lua``` files

**Create discipline file**

```bash
vim discipline.lua
```
[discipline.lua](https://github.com/marhiru/vim-setup/blob/main/zero/discipline.lua)

**Create hsl theme file**

```bash
vim discipline.lua
```
[hsl.lua](https://github.com/marhiru/vim-setup/blob/main/zero/hsl.lua)

**Create lsp file**

```bash
vim discipline.lua
```
[lsp.lua](https://github.com/marhiru/vim-setup/blob/main/zero/lsp.lua)



## After completing all theses steps, your are safe to type on your terminal

```bash
vim
```

### And your lazyvim will auto-configure based on config files, thats all! Keep safe
