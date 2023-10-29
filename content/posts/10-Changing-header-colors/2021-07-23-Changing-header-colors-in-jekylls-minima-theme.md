---
title:  "Changing Header Colors in Jekyll's Minima Theme"
date:   2021-07-30 09:58:59 +0000

draft: false
images: []

lightgallery: true

toc: false

categories: [STATIC SITE GENERATORS]
tags: [jekyll, "Minima theme"]
---

Jekyll supports a range of [themes](http://jekyllthemes.org/) and while I have tried a few I decided to use Jekyll's default Jekyll theme, 'Minima', which this site is based on. It works well out of the box. However, over time I have made a few changes.

The most recent change was with the sites sub-headings.  I had been using H2 headings in markdown but always felt they were too large.  If I used H3 headings then sub-headings seemed to get lost in the text!   The simple solution was to change the color of the H3 headings -- the blue makes the H3 headings more visible.  The image below shows the before and after.

### Before...

![Post with H3](https://imgur.com/IF5u3jH.png#center)

### After...



![Post with H2 (blue)](https://imgur.com/7zRmpIA.png#center)

For me the headings are now clearer.

To achieve the above you need to override the minima's default css file. Create a file 'assets/main.scss' with the following content:

```
---
---

@import "{{ site.theme }}";

  h3 {
    color: #1756a9;
  }

```

The hex code, #1756a9, can be changed to whichever color is preferred... I'm still not sure about the blue!!


**Update:**

I decided to keep with the colour but changed the fonts to bold.  The change to the default css file is as follows:

```
---
---

@import "{{ site.theme }}";

h3 {
  color: #1756a9;
  font-weight: 700;
}

```
