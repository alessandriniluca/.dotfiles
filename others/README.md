# Packages and positions of config
## Wofi
- package: [click here](https://archlinux.org/packages/extra/x86_64/wofi/)
- config position: `$XDG_CONFIG_HOME/wofi/` (default to: `~/.config/wofi/`). Name of the files: `color`, `config`, `style.css`.
## Kitty
- package: [click here](https://archlinux.org/packages/extra/x86_64/kitty/)
- config position: see [here](https://sw.kovidgoyal.net/kitty/conf/), it is: `~/.config/kitty/`, the name of the config file is `kitty.conf`.
## Waybar
- package: [click here](https://archlinux.org/packages/extra/x86_64/waybar/)
- config position: ` $XDG_CONFIG_HOME/waybar/`, which defaults to `~/.config/waybar/`, and the names of the files are: `config`, `style.css`.
- Other needed programs:
    - [pavucontrol](https://archlinux.org/packages/extra/x86_64/pavucontrol/)
    - [nmtui](https://man.archlinux.org/man/nmtui.1) (should come with `networkmanager`)
    - [bluetuith](https://aur.archlinux.org/packages/bluetuith-bin) to handle bluetooth
## Avizo
- package: [click here](https://aur.archlinux.org/packages/avizo)
- config position: not yer configured
## swaylock
Manages the lock screen.
- package: [click here](https://archlinux.org/packages/extra/x86_64/swaylock/)
- config position: ` $XDG_CONFIG_HOME/swaylock/`, which defaults to `~/.config/swaylock`

Be sure to include also the folder "scrips"
# Other utilities
## bluetuith
Manages bluetooth connections: [click here](https://aur.archlinux.org/packages/bluetuith-bin)
## nmtui
Manages network connections. Comes with `networkmanager` ([click here](https://man.archlinux.org/man/nmtui.1))