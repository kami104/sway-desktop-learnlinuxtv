# Sway Desktop Enviroment from [Learn Linux TV](https://www.youtube.com/channel/UCxQKHvKbmSzGMvUrVtJYnUA)
This repository is based on the Sway Desktop Enviroment setup done by Jay Lacroix  from Learn Linux TV

> [!WARNING]
> #### Use this repository under your own responsability. I'm not a professional programmer, just an ammateur with AI and free time.

<br/>

See the [official guide](https://www.learnlinux.tv/how-i-set-up-the-sway-window-manager-on-debian-12/) from Learn Linux TV and the official video:

[![official video](https://img.youtube.com/vi/e7bezUA6G4g/hqdefault.jpg)](https://youtu.be/e7bezUA6G4g)


## Table of contents
   1. [Prerequisites.](#prerequisites)
   2. [One command deploy (Work in progress).](#one-command-deploy)
   3. [Manual installation](#manual-installation)
      1. [Installing dependencies](#installing-dependencies)
      2. [Copying configuration files](#copying-configuration-files)
      3. [Making sure all scripts are executable]()

<br/>

## Prerequisites.
This guide assumes:
  - You have a Debian 12 machine.
  - You have installed Debian's "standard system utilities" in that machine.
    - <img src="https://i.sstatic.net/sNonc.png" alt="Debian standard system utilities" width="400"/>
  - You have a user with sudo privileges (root user is not valid).

> [!NOTE]
> See [this repository](https://github.com/kami104/Debian-shell-scripts/tree/main?tab=readme-ov-file#script-to-create-a-new-sudo-user-and-remove-root-login-if-it-is-enabled) to create a user like that if you don't have it.

<br/>

## One command deploy.

> [!WARNING]
> This section is work in progress.

<br/>

## Manual installation.

The next steps follow the guide the video indicated above:

### Installing dependencies

We install the necessary dependencies and create the necessary folders with these commands:
```bash
sudo apt install alacritty light sway swaybg swayidle swayimg swaylock waybar wofi fonts-font-awesome
mkdir -p ~/.config/sway ~/.config/waybar ~/.config/wofi
```

### Copying configuration files

Now we copy the contents of the forlder [sway](/.config/sway), [waybar](/.config/waybar), and [wofi](/.config/wofi) in this repository into the folders we have already creted in our machine.
