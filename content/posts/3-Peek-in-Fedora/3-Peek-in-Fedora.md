---
title:  "Peek in Fedora"
date:   2021-01-21 10:53:59 +0000
draft: false
images: []

lightgallery: true

toc: false

categories: [LINUX]
tags: [fedora, software]
---

[Peek](https://github.com/phw/peek) is an open source screen recorder for producing gif's.  It has an easy to use interface.  Once installed you open the app, position the see through frame over the part of the screen you want to record, and then press the record button...an example...

![gif](https://i.imgur.com/fpcy0ye.gif#center)

When you have finished recording you press 'stop' and finally give the .gif file a name.

The current Peek version:

\
![about-peek](/posts/3-Peek-in-Fedora/about-peek.png#center)



## Installing Peek

To install Peek on Fedora open a terminal and type:
```bash
$ sudo dnf install Peek
```

When opening the app for the first time you may get an error message

\
![error-message](/posts/3-Peek-in-Fedora/peek-ffmpeg.png#center)

If this happens then in your terminal type:
```bash
$ sudo dnf install ffmpeg
```
\
Opening the app should now work.

\
![peek-screen](/posts/3-Peek-in-Fedora/peek-screen.png#center)
