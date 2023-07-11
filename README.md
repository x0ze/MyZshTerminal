Custom [oh-my-zsh](https://ohmyz.sh/) theme with [Powerlevel10k](https://github.com/romkatv/powerlevel10k/tree/master)

## Installation

Install zsh if not already installed. To check :
```bash
echo $SHELL
```

Command to install zsh in Debian. [Installation documentation](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)
```bash
sudo apt install zsh
```

 Install oh-my-zsh. 
 >This is a delightful, open source, community-driven framework for managing your Zsh configuration.
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
Reboot after the installation

## Zsh config

Copy my `.zshrc` file on your `~` and load it by the command
```bash
source ~/.zshrc
```

OR configure manually 

### Import History
In your `~./zshrc` file :
```config
# User configuration
HISTFILE=~/.zsh_history
HISTSIZE=999999999
SAVEHIST=$HISTSIZE
setopt inc_append_history
setopt share_history
```
## Plugins
In your `~./zshrc` file if not already in:
```config
plugins=(
        git
        docker
        zsh-autosuggestions
        zsh-syntax-highlighting
        )
```
[List of plugins]([https://github.com/ohmyzsh/ohmyzsh/wiki/Plugins](https://github.com/ohmyzsh/ohmyzsh/wiki/Plugins))


### zsh-autosuggestions install
> Autosuggestions of commands
```bash
git clone https://github.com/zsh-users/zsh-autosuggestions \
  ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

### zsh-syntax-highlighting
> Highlight commands
```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git \
  ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```
## Themes
> Powerlevel10k is a theme for Zsh. It emphasizes speed, flexibility and out-of-the-box experience [https://github.com/romkatv/powerlevel10k](https://github.com/romkatv/powerlevel10k)
```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git \
  ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```
In your `~/.zshrc` file:
```bash
ZSH_THEME="powerlevel10k/powerlevel10k"
```

### Theme configuration
Copy my `.p10k.zsh` file on your `~` and load it by the command
```bash
source ~/.p10k.zsh
```

OR configure manually 

When ZSH_THEME is set configure P10K
```bash
p10k configure
```


