# Landotfiles
## Index
- [Notes](#notes)
- [Repository purpose](#repository-purpose)
- [Wallpaper](#wallpaper)
- [Other Utilities](#other-utilities)
    - [Screenshots](#screenshots)
    - [Power-Profiles For Laptop Power Management](#power-profiles-for-laptop-power-management)
    - [Spicetify](#spicetify)
- [Roadmap](#roadmap)
- [Problems I am aware of](#problems-i-am-aware-of)
## Notes
**This is still under very active development. Up to now, files are really "dirty"** (I may have not followed good rules, such as parametrization), **and some may not work**. Why? Because I am still experimenting with this setup, and I still need to increase my desktop pc capacity before installing arch linux also on it. **So, take inspiration, but at you own risk**.

Why does this repo start with a dot (".")? Because I usually leave it in the home directory (with a clone), and I want this to be hidden: it will be not visible. What I usually do then, is to [symlink](https://www.freecodecamp.org/news/symlink-tutorial-in-linux-how-to-create-and-remove-a-symbolic-link/) each folder where needed.
## Repository purpose
This repository contains my dotfiles, and is subdivided in
- Desktop: dotfiles for the desktop pc (not yet set up)
- Laptop: dotfiles for the laptop pc
- Others: things that probably will be in common (such as OSD, lockscreen, and other stuff)

Each subfolder has other READMEs that explains the purpose of each thing, and the link to guide, arch package, and possibly also its config file names.

## Wallpaper
[Click here](https://www.wallpaperflare.com/digital-digital-art-artwork-illustration-abstract-neon-wallpaper-gjjgo) for the wallpaper.

## Other Utilities

### Screenshots
For the screenshots, following the [Hyprland FAQ's page](https://wiki.hyprland.org/FAQ/#how-do-i-screenshot), it is sufficient to install [grim](https://archlinux.org/packages/extra/x86_64/grim/) and [slurp](https://archlinux.org/packages/extra/x86_64/slurp/). After this, just insert the keybinding suggested on the webpage in the `hypr.conf` file (at the moment has been added as `super`+`shift`+`P`).

### Power profiles for laptop power management
For power management at the moment I'm using [power-profiles-daemon](https://archlinux.org/packages/?name=power-profiles-daemon), which comes with `powerprofilesctl`, a CLI utility to control it.

### Spicetify
Spicetify is needed to create a custom theme for Spotify. At the moment, I am using a pre-built theme. The link to the website [is this](https://spicetify.app/docs/advanced-usage/installation), and as mentioned there you can simply download it by typing:
```
yay -S spicetify-cli
```
On Linux, you have also to give some permissions, specified [here](https://spicetify.app/docs/advanced-usage/installation/#spotify-installed-from-aur) (for convenience are reported in the following lines)
```
sudo chmod a+wr /opt/spotify
sudo chmod a+wr /opt/spotify/Apps -R
```
- **Spicetify themes**: type `git clone https://github.com/spicetify/spicetify-themes.git`, and copy the interested theme folder with a dynamic link into the folder `/home/<user>/.config/spicetify/Themes` (just type: `ln -s /path/to/cloned/spicetify-themes/<theme_folder_name> /home/<user>/.config/spicetify/Themes/<theme_folder_name>`). Then run the following commands: `spicetify config current_theme <theme_folder_name>`, `spicetify backup apply`. The dynamic link is useful, since you may want to keep up to date the repository with the topgrade toml file.
- **Other custom themes**: first give a try to the spicetify's ones. I'm currently using one of [catppuccin](https://github.com/catppuccin/spicetify.git). Clone their repo, and copy it with a dynamic link in the same folder (use a dynamic link for the same reason specified above): `ln -s /path/to/spicetify/catppuccin /home/<user>/.config/spicetify/Themes/catppuccin`. Once done that, you need to specify the color scheme with `spicetify config color_scheme <color-scheme>`, in my case `<color-scheme>` is `mocha`. Then `spicetify apply`.

### Chuck Norris Quote in terminal
Reference: [click here](https://github.com/ohmyzsh/ohmyzsh/blob/master/plugins/chucknorris/).

Dependencies:
- [Fortune](https://archlinux.org/packages/?name=fortune-mod)
- [Cowsay](https://archlinux.org/packages/extra/any/cowsay/)

## Roadmap
Please, this roadmap may be a little bit confused or not complete. See it as my "todo list", things that comes to my mind and I say "ok *Landomix*, you need to implement this".

- [ ] swaync or mako or dunst to handle notifications (I need to study and try each one of them before choosing one).
- [ ] Authentication agent. Purpose: give somehow a nice aspect and let work without problems for example the gui of timeshift.
- [ ] test and configure swayidle also with nvidia settings.
- [ ] custom css for applications
- [ ] fix a bit the color-scheme, font sizes, and make everything parametric.
- [ ] find something with nicer GUI for wifi and bluetooth.
- [ ] Power Management CLI for waybar (hint, need to investigate [this](https://community.frame.work/t/guide-linux-battery-life-tuning/6665/37))
- [ ] Set Up swaync to have more features, like [here](https://gitlab.com/lvntcylmz/dotfiles/-/raw/main/screenshots/sway-3.png), or evaluate another bar with dropdown menu [like here](https://github.com/lauroro/hyprland-dotfiles/tree/master)

## Problems I am aware of
This section contain some problems I am aware of. E.g., "I took inspiration from a code, but I partially implemented everything, so maybe something is not working". Some problems may not have been discovered yet, so if you notice someone of them, feel free to contact me or open an issue.
- [ ] the `sleep.sh` contains a `swayidle` command, but `swayidle` is not configured yet. Before of that, I want to solve the notification question, and I need to understand better how suspension works with Nvidia (my laptop needs to run everything across the Nvidia GPU, hence I want to deepen this question a little bit before proceding).