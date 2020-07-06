## Steps

1. `git clone https://github.com/thecalvinchan/config.git`
  - This should also initialize and update all submodules
  - If you cloned without `--recursive` flag, run the following:
    - `git submodule init`
    - `git submodule update`
1. Install [oh my zsh](https://github.com/robbyrussell/oh-my-zsh)
  - `sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"`
1. Install neovim
  - `brew install neovim` 
1. Install [vim-plug](https://github.com/junegunn/vim-plug) for neovim
  - `sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'`
1. Make sure yarn is installed, COC is dependent on yarn
  - `brew install yarn`
1. Install FD
  - `brew install fd`
1. Install [fzf](https://github.com/junegunn/fzf)
  - `. ./vendor/fzf/install`
4. Install [FD](https://github.com/sharkdp/fd)
  - `brew install fd`

## FD and FZF

[FD](https://github.com/sharkdp/fd) is a find alternative used by fzf to find
files while respecting `.gitignore`

```
fd --type f | fzf
```

## Download

[Inconsolata Font](http://www.levien.com/type/myfonts/inconsolata.html)

zsh theme: frisk
