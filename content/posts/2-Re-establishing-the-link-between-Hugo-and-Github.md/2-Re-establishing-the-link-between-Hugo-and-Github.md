---
title:  "Re-establishing the link between Hugo and Github"
date:   2020-12-30 11:53:59 +0000

draft: false
images: []

lightgallery: true

toc:
  auto: false

categories: [STATIC SITE GENERATORS]
tags: [hugo, github]
---

This post assumes you have already built a site using Hugo, that you have a local version of your site and are pushing changes to Github where it is being hosted.  I am fairly new to GitHub so when changing computers I was a little uncertain on how to re-establish the link with GitHub.  The following are the steps I went through.

## Background
Here is some additional information on my set-up.  I use a script (`./deploy.sh`) to push changes through to GitHub and this can be found on the [Hugo site](https://gohugo.io/hosting-and-deployment/hosting-on-github/#put-it-into-a-script).  My local folder structure, which I think is pretty standard, is shown below and includes the **deploy.sh** script. The script pushes the Public folder through to my GitHub repository, which is where this site is hosted.

\
![Folder structure](/posts/2-Re-establishing-the-link-between-Hugo-and-Github.md/folder-structure.png "Folder structure")

## Steps to Reconnect to GitHub

### Step 1 - Setting things up
a) To be safe it is probably worth cloning your GitHub repository first... just in case you mess things up!  To clone your local GitHub repository go to your GitHub repository and copy the link.

\
![GitHub-repository](/posts/2-Re-establishing-the-link-between-Hugo-and-Github.md/GitHub-repository.png "GitHub-repository")

Once you have copied the link open a terminal and type:
```bash
$ git clone https://github.com/<USERNAME>/<USERNAME>.github.io.git
```


b) Create a copy of your existing local site folder.  There are various ways to do this but for me I simply copied the whole of my **blog** folder over to Google Drive.

c) If you have not already done so install Hugo on your new computer.  For me, using Manjaro I needed to open a terminal:

```bash
$ sudo pacman -S hugo
```

d) Again, in the terminal you are going to create a new Hugo site.  I decided to keep the folder name exactly the same as my orginal.

```bash
$ hugo new site blog
```

e) Go in to the folder which you have just created and delete the contents!!  The folder will now be empty.

f) Download the folder which you saved in b) above.  Copy the contents across to the 'blog' folder you created in d).  The content of the folder should look similar to the image shown in the **Background** section above.

### Step 2 - Re-establishing the link with GitHub
The following tasks need to be completed in a terminal.  The commands do the following:

1. The first command initialises the git repository; 
2. The second command makes the deploy.sh script executable; 
3. The third completely removes the public directory; 
4. The fourth creates a git submodule and as the Hugo site [states](https://gohugo.io/hosting-and-deployment/hosting-on-github/#step-by-step-instructions) when you now "run the hugo command to build your site to public, the created public directory will have a different remote origin (i.e. hosted GitHub repository)"; and
5. The final command will run the script and push changes to your GitHub account.  Note that when running the last command you will be prompted for your GitHub username and password.

```bash
$ git init
$ chmod +x deploy.sh
$ rm -rf public
$ git submodule add -b master https://github.com/<USERNAME>/<USERNAME>.github.io.git public
$ ./deploy.sh "your optional comment"
```
It is worth testing the deploy script again with a minor change to your local site to see if it gets pushed through to your site.

