# This are my config files for my Arch rice. 
I am not a linux geek let alone an Arch expert so take my config files with a grain of salt.

## This repo has config file for:
- zsh
- vim
- tmux
- dmenu
- polybar
- picom
- neofetch
- kitty
- i3
> My `i3` uses `dmenu` as the dynamic menu (basically a launcher for all menu-items i.e. `firefox`). You can launch `dmenu` using `Mod3 + d` (Mod4 is the super key). `dmenu` is in another repository just clone [this](https://github.com/Philiks/dmenu.git) or you can build your own by applying different patches from [here](https://tools.suckless.org/dmenu/patches/). 

## Dependencies
### For zsh
**[zsh git-prompt](https://github.com/git/git/blob/master/contrib/completion/git-prompt.sh)**<br />
Put this file in /usr/share/zsh/plugins or you can edit the `source` statement inside `.zshrc`.<br /><br />
**[zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)**<br />
Follow the [INSTALL.md](https://github.com/zsh-users/zsh-syntax-highlighting/blob/master/INSTALL.md) then `cp` the `zsh-syntax-highlighting` directory inside src/ directory to /usr/share/zsh/plugins.<br /><br />
**[imagemagick](https://imagemagick.org/script/download.php)** or for **[arch-based distros](https://archlinux.org/packages/?name=imagemagick)**<br />
You should also have `kitty` for `alias icat` to work.
### For Polybar
Put the `launch.sh` and `config` under `.config/polybar`.
**[siji-ng](https://aur.archlinux.org/packages/siji-ng/)**<br />
This siji font fixes the `warn: Dropping unmatched character `. Install this package from AUR if you're using Arch or Arch-based distro.<br /><br />
**[fontawesome-free-5.15.4.zip](https://use.fontawesome.com/releases/v5.15.4/fontawesome-free-5.15.4-desktop.zip)**<br />
This is the fontawesome zip file. Run `$ unzip fontawesome-free-5.15.4-desktop.zip` to extract the compressed file. Then run:
```
$ sudo mkdir /usr/share/licences/fontawesome
$ sudo mkdir /usr/share/fonts/OTF
$ sudo mv ./fontawesome-free-5.15.4-desktop/LICENSE.txt /usr/share/licences/fontawesome
$ sudo mv ./fontawesome-free-5.15.4-desktop/otfs/Font\ Awesome\ 5\ Brands-Regular-400.otf /usr/share/fonts/OTF
$ sudo mv ./fontawesome-free-5.15.4-desktop/otfs/Font\ Awesome\ 5\ Free-Regular-400.otf /usr/share/fonts/OTF
$ sudo mv ./fontawesome-free-5.15.4-desktop/otfs/Font\ Awesome\ 5\ Free-Solid-900.otf /usr/share/fonts/OTF
```
> Note that you must have `unzip` to decompress the zip file. Although you can still use other decompresser package.
> Note that the directories your moving the files into must be created prior the `mv` command otherwise it will move the file but rename it with the last *folder*. i.e. moving `./fontawesome-free-5.15.4-desktop/LICENSE.txt` to `/usr/share/licences/fontawesome` whilst not having the `fontawesome` directory will rename the `LICENSE.txt` to `fontawesome`.
### For i3
**[escrotum](https://github.com/Roger/escrotum)**<br />
Install this from the AUR or follow their [installation](https://github.com/Roger/escrotum#install) guide.
### For tmux
> If `tmux` won't load the config file, place it inside *home* directory `~` then change the name to `.tmux.conf`. Lastly, run `tmux kill-server` to kill all tmux sessions.
