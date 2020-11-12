# suckless.CentOS
WieWaldi's collection of suckless applications and other simple tools adapted to
a minimal installation of CentOS. Yes, the name of this repository may be kinda
missleading since it doesn't contain suckless implementations only but other
stuff as well. This repo targets specially and only a minimal installation of
CentOS 7/8.

## Motivation ...
... is to get a CentOS minimal installation equiped with a suckless graphical
user interface in pretty much no time and hassle using a script for building
and installation.
I'm convinced that RedHatEL/CentOS is one of the best GNU/Linux distributions
and very well suited for company and business use. In my case, I'm running many
RedHatEL/CentOS servers at the back office and on some workstations as well.
I'm running security and data integrity tools for monitoring and alerting on
file & directory changes on all of my servers and workstations. The alarm bells
go off every time something gets changed besides the home directory. Hence I'm
installing most of these applications in my home directory.

## Requirements
A minimal installation of CentOS 8/7. All needed repositories and packages will
get installed during preparation. Don't forget to update your system right after
installation.

## Installation
Installation is split up in two parts. First you have to run the preparation
script as root. This will prepare your system by adding needed repositories and
packages and copying configuration files. During the preparation you will be
asked if you want to have the Google Chrome repository added.

Then you log in with your user account at the console and run the setup script.
This will compile and install a bunch of applications. 

At that point I suggest to install my [.dotfiles](https://github.com/WieWaldi/.dotfiles)
as well.

Just to make that clear. You don't have to use the setup script. You may walk
through all sub directories and pick what you want to build and install.

To get slock working you have to set uid correctly.
```
sudo chown root:root ~/.local/bin/slock
sudo chmod u+s ~/.local/bin/slock
```

## Contents
This repository cotains the folloing applications. For convenience most of the
suckless.org applications have been patched already.
- **compton** - a compositor for X11
- **dmenu** - dynamic menu (Version 5.0) contains the following patches.
  - dmenu-borderoption-20200217-bf60a1e.diff
  - dmenu-center-20200111-8cd37e1.diff
  - dmenu-mousesupport-5.0.diff
  - dmenu-mousesupporthoverbgcol-5.0.diff
  - dmenu-numbers-4.9.diff
  - dmenu-xresources-4.9.diff
- **dunst** - A customizable and lightweight notification-daemon
- **dwm** - dynamic window manager (Version 6.2) contains the following patches.
  - dwm-autostart-20200610-cb3f58a.diff
  - dwm-barpadding-20200720-bb2e722.diff
  - dwm-cfacts-20200913-61bb8b2.diff
  - dwm-colorbar-6.2.diff
  - dwm-fakefullscreen-20170508-ceac8c9.diff
  - dwm-fibonacci-20200418-c82db69.diff
  - dwm-fullgaps-20200508-7b77734.diff
  - dwm-monoclesymbol-6.2.diff
  - dwm-movestack-6.1.diff
  - dwm-notitle-6.2.diff
  - dwm-pertag-20200914-61bb8b2.diff
  - dwm-resizecorners-6.2.diff
  - dwm-xresources-6.2.diff
- **feh** — image viewer and cataloguer
- **lsw** - list windows
- **maim** - make image
- **rotwall** - rotate wallpapers
- **slock** — simple X screen locker (Version 1.4) contains the following patches.
  - slock-message-20191002-b46028b.diff
  - slock-xresources-20191126-53e56c7.diff
- **slop** - select operation
- **sselp** - Simple X selection printer
- **st** - simple terminal (Version 0.8.4) contains the following patches.
  - st-alpha-0.8.2.diff
  - st-blinking_cursor-20200531-a2a7044.diff
  - st-bold-is-not-bright-20190127-3be4cf1.diff
  - st-iso14755-0.8.3.diff
  - st-iso14755-20180911-67d0cb6.diff
  - st-scrollback-20200419-72e3f6c.diff
  - st-scrollback-mouse-20191024-a2c479c.diff
  - st-xresources-20200604-9ba7ecf.diff
- **surf** - simple webkit-based browser (Version 2.0) contains the following patches.
  - surf-bookmarks-20170722-723ff26.diff
  - surf-dlconsole-20190919-d068a38.diff
  - surf-git-20170323-webkit2-searchengines.diff
  - surf-scrollmultiply-2.0.diff
- **sxiv** - Simple X Image Viewer
- **tabbed** - generic tabbed interface
- **xclickroot** - run command on button press on root window
- **xclientprop** - show condenst X client properties through xmessage
- **xdotool** - command-line X11 automation tool
- **xmenu** - menu utility for X
- **xmerge** - Merge and apply .Xresource

