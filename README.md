## XDG Directories

1. XDG_CONFIG_HOME
  - `git clone https://github.com/thecalvinchan/config.git ~/.config`
1. XDG_DATA_HOME
  - `mkdir ~/.local/share`
1. XDG_CACHE_HOME
  - `mkdir ~/.cache`

## Zsh and Oh-My-Zsh
1. Copy `.zshenv` to `$HOME`
  - `ln -s $PWD/zsh/.zshenv ~/.zshenv`
1. Install [oh my zsh](https://github.com/robbyrussell/oh-my-zsh)
  - `ZSH="$XDG_CONFIG_HOME/oh-my-zsh" sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"`
1. Create dir for `.zsh_history`
  - `mkdir $XDG_CACHE_HOME/zsh`

#### Oh-My-Zsh Plugins
1. Install zsh-nvm
  - `git clone https://github.com/lukechilds/zsh-nvm "$ZSH/custom/plugins/zsh-nvm"`
1. Install git-open
  - `git clone https://github.com/paulirish/git-open.git "$ZSH_CUSTOM/plugins/git-open"`

## Homebrew
1. Install homebrew
  - https://brew.sh
1. No need to add homebrew to path as that is taken care of in `.config/zsh/.zprofile`

## FD and FZF

[FD](https://github.com/sharkdp/fd) is a find alternative used by fzf to find
files while respecting `.gitignore`

```
fd --type f | fzf
```

1. Install [FD](https://github.com/sharkdp/fd)
  - `brew install fd`
1. Install [fzf](https://github.com/junegunn/fzf)
  - `brew install fzf`
  - To install [useful key bindings and fuzzy completion](https://github.com/junegunn/fzf#key-bindings-for-command-line):
    - `$(brew --prefix)/opt/fzf/install`
    - This will generate `.fzf.zsh`. When asked, do not add to shell configuration files, since we already handle that in `.config/zsh/.zshrc`

## Neovim
1. Install neovim
  - `brew install neovim` 
1. Install [vim-plug](https://github.com/junegunn/vim-plug) for neovim
  - `sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'`
  - Open nvim and run `:PlugInstall`
1. Install Coc Plugins
  - `cd coc/extensions && npm install`
  - This requires `npm` to be installed. `zsh-nvm` will handle installing nvm, so open a new terminal window and run `nvm install`.

## Hammerspoon
1. Install Hammerspoon
  - `brew install --cask hammerspoon`
1. [ShiftIt Spoon](https://github.com/peterklijn/hammerspoon-shiftit) shoudl already be installed
1. Change hammerspoon config directory
  - `defaults write org.hammerspoon.Hammerspoon MJConfigFile "~/.config/hammerspoon/init.lua"`
1. Make sure that Hammerspoon has [accessibility permissions](https://github.com/peterklijn/hammerspoon-shiftit#step-4)

## Fonts

[Inconsolata Font](http://www.levien.com/type/myfonts/inconsolata.html)

## Theme

[Iceberg for iTerm2](https://github.com/Arc0re/Iceberg-iTerm2)
