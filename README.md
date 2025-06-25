# Sway Desktop Enviroment setup from [Learn Linux TV](https://www.youtube.com/channel/UCxQKHvKbmSzGMvUrVtJYnUA)
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
      3. [Making all scripts executable](#making-all-scripts-executable)

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

### Installing dependencies

We install the necessary dependencies and create the necessary folders with these commands:
```bash
sudo apt update && sudo apt install -y alacritty light sway swaybg swayidle swayimg swaylock waybar wofi fonts-font-awesome git
```

> [!NOTE]
> We are also installing git to download the configuration files on the next step.

<br/>

### Copying configuration files

Now we copy the contents of the forlder [sway](/.config/sway), [waybar](/.config/waybar), and [wofi](/.config/wofi) in this repository into the folders we have already creted in our machine.
To do so, we will download this repository in the system temporary folder (`/tmp`).

```bash
cd /tmp
git clone https://github.com/kami104/sway-desktop-learnlinuxtv.git
```

Now we copy the downloaded files into the folder `~/.config/...`

```bash
cp -r /tmp/sway-desktop-learnlinuxtv/.config/sway/ ~/.config/sway/
cp -r /tmp/sway-desktop-learnlinuxtv/.config/waybar/ ~/.config/waybar/
cp -r /tmp/sway-desktop-learnlinuxtv/.config/wofi/ ~/.config/wofi/
```
> [!NOTE]
> The previous commands will also create de folders `sway`, `waybar` and `wofi` inside `~/.config/`

<br/>

### Making all scripts executable

To be sure all copied `.sh` scripts are executable, run the follow command:

```bash
chmod +x ~/.config/sway/*.sh
```
Now you can execute your Sway Desktop enviroment running the command `sway` after login.
