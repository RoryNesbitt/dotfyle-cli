dotfyle-cli
====

A command line tool to test out Neovim configs found on
[dotfyle](https://dotfyle.com) (or github)

![example](https://user-images.githubusercontent.com/33930918/266866395-ce0b89cc-a953-4208-abeb-465f03f7b752.png)

## Requirements

- fzf - dotfyle-cli is posix complient so should run anywhere as long as
[fzf](https://github.com/junegunn/fzf) is available
- git - Some features of dotfyle-cli will only work if git is available
  (install/update)

## installation

assumes you have `~/.local/bin` in your PATH, feel free to change the directory
```sh
curl -o ~/.local/bin/dotfyle https://raw.githubusercontent.com/RoryNesbitt/dotfyle-cli/main/dotfyle
```

alternatively you can clone this repo and then add that location to your PATH.
e.g.
```sh
git clone git@github.com:RoryNesbitt/dotfyle-cli ~/.local/dotfyle-cli
echo 'export PATH="$HOME/.local/dotfyle-cli:$PATH"' >> ~/.bashrc
```
This is more bloated but will make getting updates simpler, however updates are
likely to be rare so this is not the recommended method of installation.

## Using dotfyle-cli

### Config installation

start by installing some configs
```sh
dotfyle install https://dotfyle.com/codicocodes/dotfiles-nvim
dotfyle install https://github.com/folke/dot/tree/master/nvim
dotfyle install RoryNesbitt/RNvim
```

### Running Neovim

Then select which one you want to start Neovim with using
```sh
dotfyle
# or
dotfyle run
```
From here the last used config will become the default, and to select a new on
use
```sh
dotfyle run --ask
```

### Getting more help/config management

dotfyle-cli can also remove or update configs, check out the options with
```sh
dotfyle --help
```

On removing a config the related files are also removed from
- ~/.config/neovim-configs
- ~/.cache/neovim-configs
- ~/.local/share/neovim-configs
- ~/.local/state/neovim-configs
