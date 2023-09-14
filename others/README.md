# Packages and positions of config
## Index
- [What is](#what-is)
- [Packages](#packages)
    - [Wofi](#wofi)
    - [Kitty](#kitty)
    - [Waybar](#waybar)
    - [Avizo](#avizo)
    - [Swaylock-effects](#swaylock-effects)
    - [Swayidle](#swayidle)
## What is
This repo contains config and links to packages common to both desktop and laptop (**waybar could be moved and splitted into laptop version and desktop version, due to different monitor sizes**). Generally, for each package is reported:
- its purpose
- arch linux package link
- config folder position
## Packages
### Wofi
Wofi is a launcher application, suggested [here](https://wiki.hyprland.org/Useful-Utilities/App-Launchers/) in the hyprland guide.
- package: [click here](https://archlinux.org/packages/extra/x86_64/wofi/)
- config position: `$XDG_CONFIG_HOME/wofi/` (default to: `~/.config/wofi/`). Name of the files: `color`, `config`, `style.css`.
### Kitty
Kitty is the "default terminal emulator" of hyprland (at the time of writing this guide, mentioned [here](https://wiki.hyprland.org/0.21.0beta/Getting-Started/Master-Tutorial/)).
- package: [click here](https://archlinux.org/packages/extra/x86_64/kitty/)
- config position: see [here](https://sw.kovidgoyal.net/kitty/conf/), it is: `~/.config/kitty/`, the name of the config file is `kitty.conf`.
### Waybar
Waybar is a status bar, suggested [here](https://wiki.hyprland.org/Useful-Utilities/Status-Bars/).
- package: [click here](https://archlinux.org/packages/extra/x86_64/waybar/)
- config position: ` $XDG_CONFIG_HOME/waybar/`, which defaults to `~/.config/waybar/`, and the names of the files are: `config`, `style.css`.
- Other needed programs:
    - [pavucontrol](https://archlinux.org/packages/extra/x86_64/pavucontrol/): needed to handle in an easy way volumes of input and output separately.
    - [nmtui](https://man.archlinux.org/man/nmtui.1) (should come with `networkmanager`): needed to have a GUI like experience from terminal, for network connections management.
    - [bluetuith](https://aur.archlinux.org/packages/bluetuith-bin): needed to have a GUI like experience from terminal, for Bluetooth connections management.
    - For the script [mediaplayer.py](https://github.com/Alexays/Waybar/blob/master/resources/custom_modules/mediaplayer.py), the suggestion came from a [reddit post](https://www.reddit.com/r/swaywm/comments/ni0vso/waybar_spotify_tracktitle/).
### Avizo
Avizo is one of the possible OSD, mentioned in the [awesome hyprland](https://github.com/hyprland-community/awesome-hyprland) repository.
- package: [click here](https://aur.archlinux.org/packages/avizo)
- config position: avizo still needs to be configured, up to now is included "as it is".
### swaylock-effects
Manages the lock screen. Why not simply [swaylock](https://archlinux.org/packages/extra/x86_64/swaylock/)? Because with swaylock-effects we have more possibilities of personalization (e.g., we can include in a simple way a clock).
- package: [click here](https://aur.archlinux.org/packages/swaylock-effects)
- config position: ` $XDG_CONFIG_HOME/swaylock/`, which defaults to `~/.config/swaylock`

Be sure to include also the folder "scripts"
### Swayidle
**To be configured**