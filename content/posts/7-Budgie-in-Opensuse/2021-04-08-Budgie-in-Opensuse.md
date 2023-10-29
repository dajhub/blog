---
title:  "Budgie Desktop in Opensuse"
date:   2021-04-08 09:53:59 +0000

draft: false
images: []

lightgallery: true

toc: false

categories: [LINUX]
tags: [budgie, opensuse, desktops]
---

Budgie Desktop is the default desktop on the [Solus Linux distrubution](https://getsol.us/solus/about/) and is a fantastic desktop.  It can also be installed on other operating systems.  This post looks at how to install the Budgie desktop on [Opensuse Tumbleweed](https://get.opensuse.org/tumbleweed).  It assumes that you have downloaded the ISO and installed on a USB using, for example, [Etcher](https://www.etcher.net/).

## Installing Opensuse Tumbleweed

The steps to installing Opensuse Tumbleweed from your USB:

1) On the first screen select "Installation"

2) Progress through the installation screens until the following screen:

![online-repository](/posts/7-Budgie-in-Opensuse/online-repository.png#center)

	Select 'Generic Desktop'.  After this step follow through the remaining screens to setup your installation, e.g. username.

3) Login in to the new generic desktop which will be icewm window manager:

![icewm](/posts/7-Budgie-in-Opensuse/icewm.png#center)

4) The first step in any fresh install is to update your system. Open a terminal (e.g. xterm) and enter the following command:

```bash
$ sudo zypper dup
```

5)  At this stage it is worth  installing [Packman](https://en.opensuse.org/SDB:Installing_codecs_from_Packman_repositories).  Packman conveniently groups several third party repositories together and is the largest group of third party packages built for openSUSE. Packman can be easily enabled via the Terminal.

```bash
$ sudo zypper addrepo -cfp 90 'https://ftp.gwdg.de/pub/linux/misc/packman/suse/openSUSE_Tumbleweed/' packman
```

6) After adding the Packman repository, it's necessary to refresh and move package updates to the Packman repository (the latter helps to avoid conflicts when packages are updated):

```bash
$ sudo zypper refresh
$ sudo zypper dist-upgrade --from packman --allow-vendor-change
```

### Install Budgie Desktop

To install the [budgie desktop](https://en.opensuse.org/Portal:Budgie) open a terminal:

```bash
$ sudo zypper install budgie-desktop
```

Once the packages have been installed log out of the desktop.  Having logged out you can then select the Budgie desktop:

![budgie-login](/posts/7-Budgie-in-Opensuse/login-budgie.png#center)

When you now log in you should see your Budgie desktop:


![budgie-desktop](/posts/7-Budgie-in-Opensuse/budgie-desktop.png#center)

You may, at this point, want to look to change the appearance of your new desktop.
