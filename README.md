## Steps

1. `git clone https://github.com/thecalvinchan/config.git`
  - This should also initialize and update all submodules
  - If you cloned without `--recursive` flag, run the following:
    - `git submodule init`
    - `git submodule update`
1. Set XDG_CONFIG_HOME
  - `export XDG_CONFIG_HOME=$HOME/.config`

## Zsh and Oh-My-Zsh
1. Install [oh my zsh](https://github.com/robbyrussell/oh-my-zsh)
  - `ZSH="$XDG_CONFIG_HOME/oh-my-zsh" sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"`
1. Copy `.zshenv` to `$HOME`
  - `ln -s $PWD/zsh/.zshenv ~/.zshenv`
1. Install zsh-nvm
  - `git clone https://github.com/lukechilds/zsh-nvm "$ZSH/custom/plugins/zsh-nvm"`

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
