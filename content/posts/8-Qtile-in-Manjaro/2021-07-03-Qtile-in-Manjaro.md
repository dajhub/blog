---
title:  "Qtile in Manjaro"
date:   2021-07-03 09:53:59 +0000

draft: false
images: []

lightgallery: true

toc: false

categories: [LINUX]
tags: [manjaro, window manager, qtile]
---

This post takes you briefly through how [Qtile](http://www.qtile.org/), a window manager, can be installed on Manjaro.  Qtile is based on Python.  The instructions assume that XFCE4 is already installed.  In my case I have [Manjaro XFCE](https://manjaro.org/download/).

![Qtile](https://imgur.com/gLUB4GH.png)

## Installing Qtile (on Manjaro or Arch) and Loading my Configuration Files

The first step is to install Qtile:

```bash
$ sudo pacman -S qtile
```

Qtile will, when it loads, look for a script in '~/.config/qtile/config.py' by default.  The config file for my setup can be found in my [GitHub repository](https://github.com/dajhub/dotfiles/tree/master/qtile).  The GitHub config.py file can be copied across to your own path (i.e. ~/.config/qtile/config.py). In the same folder you can also copy across:
- icon folder
- autostart.sh which autostarts picom (transparency and rounded corners).  You will also need to make sure that this is an executable file, i.e. that it can be run as a program.  This can be done via the command line or GUI method.  The following is the latter:

	- Right-click the file and select Properties.
	- Go to the permissions tab, then tick the box Execute: [ ] Allow this file to run as a program in Thunar.

![Executable-file](https://imgur.com/MwfSE6G.png#center)

**Please note that these configuration files are still work in process!!  Use at your own peril!!**

Some additional items which the config file will require include:

a) [Picom](https://github.com/jonaburg/picom) - the GitHub site (in the link) shows how the compositor can be installed.  The picom config file needs to be placed in the '~/.config' folder.  My config for picom can be found on my [GitHub](https://github.com/dajhub/dotfiles) repository.

b) [Alacritty](https://github.com/alacritty/alacritty) is used as the terminal and can be downloaded as follows:

```bash
$ sudo pacman -S alacritty
```

The terminal can be extensively configured.  The config file needs to be placed in a folder... '~/.config/alacritty'.  My alacritty config can be found in my [GitHub](https://github.com/dajhub/dotfiles/tree/master/alacritty) repository.  The font being used is 'Source Code Pro' but this can easily be changed in the alacritty.yml file.  Whichever font you choose just ensure that it is installed in your system.

c) Wallpapers - the Qtile config.py file will look for wallpapers at '~/Pictures/wallpapers/'.  Again, if needed, the wallpaper folder from my GitHub repository can be downloaded.

d) The font being used in the bar is 'SF Pro Display',i.e. otf-san-francisco.  You may need to install the font.

f) The icons being used in the bar come from [Font Awesome](https://fontawesome.com/) - 'ttf-font awesome'

g) [Rofi](https://github.com/davatorium/rofi) is a launcher that provides a list of options where one or more can be selected. This can either be ***"running an application, selecting a window, or options provided by an external script."***  Mine is just a simple application launcher.

![Rofi](https://imgur.com/NS82Juv.png)

To install Rofi:

```bash
$ sudo pacman -S rofi
```

If you want to copy my rofi [files](https://github.com/dajhub/dotfiles/tree/master/rofi_) across then these need to be copied into a '~/.config/rofi' folder.  You may need to create the 'rofi' folder first.

The key binding for launching rofi is 'Alt+Space'.  This can be changed in the 'config.py' file.

It is worth noting that some of my key bindings for Qtile may be different from the [default key bindings](http://docs.qtile.org/en/stable/manual/config/index.html#key-bindings).
