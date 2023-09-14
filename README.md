# Landotfiles
## Index
- [Notes](#notes)
- [Repository purpose](#repository-purpose)
- [Wallpaper](#wallpaper)
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
## Roadmap
Please, this roadmap may be a little bit confused or not complete. See it as my "todo list", things that comes to my mind and I say "ok *Landomix*, you need to implement this".

- [ ] swaync or mako or dunst to handle notifications (I need to study and try each one of them before choosing one).
- [ ] Authentication agent. Purpose: give somehow a nice aspect and let work without problems for example the gui of timeshift.
- [ ] test and configure swayidle also with nvidia settings.
- [ ] custom css for applications
- [ ] fix a bit the color-scheme, font sizes, and make everything parametric.
- [ ] find something with nicer GUI for wifi and bluetooth.

## Problems I am aware of
This section contain some problems I am aware of. E.g., "I took inspiration from a code, but I partially implemented everything, so maybe something is not working". Some problems may not have been discovered yet, so if you notice someone of them, feel free to contact me or open an issue.
- [ ] the `sleep.sh` contains a `swayidle` command, but `swayidle` is not configured yet. Before of that, I want to solve the notification question, and I need to understand better how suspension works with Nvidia (my laptop needs to run everything across the Nvidia GPU, hence I want to deepen this question a little bit before proceding).