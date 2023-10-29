---
title:  "Fedora Xfce | A minimal install"
date:   2022-07-25 08:58:59 +0000

draft: false
images: []

lightgallery: true

toc: false

categories: [LINUX]
tags: [fedora, desktops, xfce]
---

Fedora already offers a full [Xfce desktop](https://spins.fedoraproject.org/xfce/), which is not themed but does include a lot of applications.  The aim of this post is to look at how to do a minimal install of the desktop using Fedora's [Alternative downloads](https://alt.fedoraproject.org/).  On the 'Alt Downloads' page of Fedora, scroll down to "Everthing" and then download the iso...

![Everything](https://i.imgur.com/je5UYLM.png)


The installer will take you through all the installation stages.  Crucially, when you get to the page shown below opt for the minimal install.

![Minimal Install](https://i.imgur.com/hgdg4AJ.png)

Once your installation is complete reboot into the terminal. This will happen automatically when you reboot.  Having entered your login and password, enter the commands below. A brief explanation of some of the commands is also shown below.

```bash
$ sudo dnf update
$ sudo dnf install git
$ git clone https://github.com/dajhub/fedora
$ cd fedora
$ sudo ./1-install.sh
$ ./2-install-remainder.sh
```

The second command installs git which is needed to clone my [GitHub repository](https://github.com/dajhub/fedora).  The last two commands are the installation scripts.  It is worth taking a look at each and changing as required.

## First Installation Script

```bash
sudo ./1-install.sh
```

If you look through the [script](https://github.com/dajhub/fedora/blob/main/1-install.sh), which requires sudo privileges, it, firstly sets your hostname for the terminal and then installs:
- Required packages for a xfce desktop.
- Lightdm as a display manager and enables it.
- RPM fusion and Flathub.
- Packages which I regularly use. Change these based on your needs.  For example, you may want to install Firefox or Chromium.
- [Librewolf](https://librewolf.net/)
  
## Second Installation Script

```bash
./2-install-remainder.sh
```

This [script](https://github.com/dajhub/fedora/blob/main/2-install-remainder.sh) is optional and does not require sudo privileges.  The scripts sets up a few things for me:
- Creates a number of folders (see the script!)
- Copies across wallpapers, themes, fonts and icons

The installation script contains all the basics that allows me, with some **tweaking in the 'Settings Manager'** in the desktop, to get to a desktop which looks as follows:

![Everblush theme](https://i.imgur.com/2FhThaP.png)


The above desktop follows the [Everblush Theme](https://github.com/Everblush). 

Once the scripts have been installed, typing 'reboot' will take you to the display manager login screen and a minimal installation of Xfce.  You can then theme Xfce with your own theme or with the installed Everblush theme.

![Xfce minimal](https://i.imgur.com/tdxtdzS.png)

