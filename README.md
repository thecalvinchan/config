## XDG Directories

1. XDG_CONFIG_HOME
  - `git clone https://github.com/thecalvinchan/config.git ~/.config`
1. XDG_DATA_HOME
  - `mkdir ~/.local/share`
1. XDG_CACHE_HOME
  - `mkdir ~/.cache`

## Zsh and Oh-My-Zsh
1. Install [oh my zsh](https://github.com/robbyrussell/oh-my-zsh)
  - `ZSH="$XDG_CONFIG_HOME/oh-my-zsh" sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"`
1. Copy `.zshenv` to `$HOME`
  - `ln -s $PWD/zsh/.zshenv ~/.zshenv`
1. Create dir for `.zsh_history`
  - `mkdir $XDG_DATA_HOME/zsh`

#### Oh-My-Zsh Plugins
1. Install zsh-nvm
  - `git clone https://github.com/lukechilds/zsh-nvm "$ZSH/custom/plugins/zsh-nvm"`
1. Install git-open
  - `git clone https://github.com/paulirish/git-open.git "$ZSH_CUSTOM/plugins/git-open"`

## Neovim
1. Install neovim
  - `brew install neovim` 
1. Install [vim-plug](https://github.com/junegunn/vim-plug) for neovim
  - `sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'`

## FD
1. Install [FD](https://github.com/sharkdp/fd)
  - `brew install fd`

## FZF
1. Install [fzf](https://github.com/junegunn/fzf)
  - `. ./vendor/fzf/install`

## FD and FZF

[FD](https://github.com/sharkdp/fd) is a find alternative used by fzf to find
files while respecting `.gitignore`

```
fd --type f | fzf
```

## Fonts

[Inconsolata Font](http://www.levien.com/type/myfonts/inconsolata.html)
