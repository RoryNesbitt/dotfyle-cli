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
You will then be able to get the new version with `dotfyle upgrade`

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
Or run your last used with
```sh
dotfyle run --last-used
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
