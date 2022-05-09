# Dotfiles

[![License](https://img.shields.io/badge/License-MIT-lightgray)](/LICENSE)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.0-lightblue)](/code_of_conduct.md)
[![Conventional Commits](https://img.shields.io/badge/Conventional%20Commits-1.0.0-yellow.svg)](https://conventionalcommits.org)
[![en](https://img.shields.io/badge/lang-en-red.svg)](/README.md)
[![pt-br](https://img.shields.io/badge/lang-pt--br-green.svg)](/README.pt-br.md)
[![love](https://img.shields.io/badge/Build%20With-%F0%9F%96%A4-lightgreen)](https://callmarx.github.io)

Finally I "organized" it!

```txt
          888d                888d       ~/dotfile 888d   888d
          888d                888d       888d"     888d   888d
          888d                888d      888d              888d
          888d                888d      888d       888d   888d
    ~/dotfiles   ~/dotfiles  ~/dotfiles ~/dotfiles 888d   888d   ~/dotfiles   ~/dotfiles
   888d"  888d  888d"  "888d  888d      888d       888d   888d  888d   888d   888d
  888d    888d  888d    888d  888d      888d       888d   888d  ~/.dotfiles   ~/dotfiles
   888d"  888d  888d"  "888d  888d"     888d       888d   888d  888d                888d
    ~/dotfiles   ~/dotfiles    888d"    888d       888d   888d   ~/.dotfiles  ~/dotfiles
```

## Git
The [.gitconfig](./.gitconfig) files is kind of personal and mine isn't a big deal: it enables the
colors for commands like `$ git log`. I also defined the `develop` branch as the main and I use a
commit message template defined in [.gitmessage](./.gitmessage), which was inspired in
[Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/).

## Nerd Fonts
A Font package that I use in Tilix and Neovim. To install or read more about see:
<https://github.com/ryanoasis/nerd-fonts>.

## Oh My Zsh
I use `zsh` shell with [*Oh My Zsh*](https://github.com/ohmyzsh/ohmyzsh) manager. To check if you
have it installed in your linux and if it is defined as default shell, use:
```bash
# Check if is installed
$ zsh --version

# Check if it is the default shell. You should receive 'bin/szh'
$ echo $SHELL
```

The [.zshrc](./.zshrc) file was basically generated by *Oh My Zsh* installer, I only added some
plugins. To install it, execute:
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

I also use the [Powerlevel10k](https://github.com/romkatv/powerlevel10k#oh-my-zsh) theme (**it
should have *NerdFonts* installed!**). To add in your *Oh My Zsh*, execute:
```bash
$ git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```
Also add `ZSH_THEME="powerlevel10k/powerlevel10k"` in your `~/.zshrc`.


## Tilix Terminal Emulator
To import my setup (**it should have *Nerd Fonts* installed!**) execute:
```bash
$ dconf dump /com/gexperts/Tilix/ < tilix.dconf
```

## My Neovim like an IDE
Set of plugins and settings that I use in Neovim. To organized it (and don't let it as a giant
single file) I spread my setup in other files as you can see in [nvim/lua/user](./nvim/lua/user),
keeping [init.lua](./nvim/init.lua) simple, only to load the other configuration files.

Copy, change and use it at will. Suggestions and (polite) criticism are welcome 🤓.

**NOTE**: To use the [vim-devicons](https://github.com/ryanoasis/vim-devicons) icons you need to
install [Nerd Fonts](https://www.nerdfonts.com) and enable in your terminal emulator profile or if
you use Tilix you can use my settings as I explained before.

## Licence
Licensed under MIT, see [LICENSE](/LICENSE).

## Code of conduct
I'm committed to providing a friendly, safe, and welcoming environment for all. Please read and
respect the [code of conduct](/code_of_conduct.md).
