---
title:  "Installing Jekyll on Arch"
date:   2021-02-28 10:53:59 +0000

draft: false
images: []

lightgallery: true

toc: false

categories: [LINUX]
tags: [jekyll, arch]
---

[Jekyll](https://jekyllrb.com/) is a static open source site generator which I've used for a while in conjunction with free hosting on [GitHub](https://github.com/).  It's a great combination for hosting a free site/blog.  The instructions on the Jekyll site make it easy to install.  I've used the Jekyll instructions to install it on both Fedora and Ubuntu with few problems.  However, the set-up was a little more problematic.  These are the steps I went through to install Jekyll on Arch:

1. Install the [Jekyll prerequisites](https://jekyllrb.com/docs/installation/other-linux/#archlinux) using your terminal:

   ```bash
   $ sudo pacman -S ruby base-devel
   ```

2. Jekyll requires the installation of [gems](https://learn.cloudcannon.com/jekyll/gemfiles-and-the-bundler/) .  Still in the terminal you can add environmental variables to your shell script (`.bashrc`) to set up the gem installation path:

   ```bash
   $ echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
   $ echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
   $ echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
   $ source ~/.bashrc
   ```

3. Finally, the Jekyll gem's can be installed:

   ```bash
   $ gem install jekyll bundler
   ```


4. However, at this point, as the Jekyll bundler is being installed an error message pops up:
   
   ![Jekyll-gem-install-warning](/posts/6-jekyll-in-arch/jekyll-gem-install-warning.png#center)
   
   \
   If you now try to create a new site with this command:

   ```bash
   $ jekyll new blog
   ```

   a message appears: `bash: jekyll: command not found`

5. To correct the above:

   ```bash
   $ export PATH="/home/david/.local/share/gem/ruby/2.7.0/bin:$PATH"
   $ PATH="$PATH:$(ruby -e 'puts Gem.user_dir')/bin"
   ```

   Obviously you need to change the path in the first command to suite your own setup.

   Run:

   ```bash
   $ jekyll new blog
   ```

   The new Jekyll folder will be installed and can be found in your home directory:

    ![Jekyll-folder](/posts/6-jekyll-in-arch/jekyll-folder.png#center)

   Having created the Jekyll folder, 'blog', in your Home directory you can build the default site and check that it works.  In the terminal change the directory to `blog` (or whatever your blog folder is called) and then build:

   ```bash
   $ cd blog
   $ bundle exec jekyll serve
   ```

   In your browser paste the following into the address bar:  `http://localhost:4000`. You should see the Jekyll minima site.

    ![Jekyll-site](/posts/6-jekyll-in-arch/jekyll-site.png#center)
   