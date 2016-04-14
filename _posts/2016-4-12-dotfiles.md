---
layout: post
title: Use Github as the system backup - My dotfiles   (在Github中备份系统设置 - 我的dotfile配置)
---

In less than two weeks, I broke my operating system, twice. As a programmer, we all know it is a extremely painful process to re-install all the dependencies, set up configurations, etc. However, we have to face such disasters now and then. I erroneously remove "libglib*" when I tried to install gimp, the alternative of Photoshop on Linux. Unfortunately, it is notoriously difficult to build from source, which is another long story. However, I am a little bit luckier this time because I started to document part of my working enviroments since my hard disk broke down two weeks ago (remember I told you that I broke my OS twice in two weeks, sad story...). 

![]({{ site.baseurl }}/images/project_dotfiles.png)

This project is still under construction, which basically contains my editor settings, frequently-used softwares and bash files. It will recover my editor settings and install the latest version of cmake (3.5.1), sublime text 3(3103), meshlab, which might be helpful for Graphics/CV guys like me. It may be unwise to directly run install.sh script if you don't know what it does, since it installs several dependencies for my daily development (c++, science, graphics, computer vision, ...). One thing particularly useful is my *.vimrc* settings (if you also use the vim editor), which is well tested and very easy to configure. Just *cd* into the editor folder and type:  

```
cp vimrc ~/.vimrc   # copy the vim configuration file
rm -rf ~/.vim       # delete old vim settings if any 
rsync -av vim ~/    # copy the new one
mv ~/vim ~/.vim     # change the folder name
```

Below are the vim addons that it automically installs:  
* ctrlsf.vim: An ack/ag/pt powered code search and view tool.
* OmniCppComplete: C/C++ omni-completion with ctags database.
* indexer: Auto-generate tags for all files of project(s) and keep tags up-to-date.
* pathogen.vim: It makes it super easy to install plugins and runtime files in their own private directories.
* vim-signature: vim-signature is a plugin to place, toggle and display marks.
* vimprj: Plugin for managing options for different projects.


For more instructions head over to the [dotfiles](https://github.com/hlzz/dotfiles) on GitHub.
