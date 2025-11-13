# Installation Information

## Generic

### Decrypt backup
Decrypt and mounts LUKS encrypted LVM drive:
```bash
$ sudo cryptsetup luksOpen /dev/sda3 backup
$ sudo mkdir -vp /mnt/backup/{root,home}
$ sudo mount /dev/archvg/arch_home /mnt/backup_home
$ sudo mount /dev/archvg/arch_root /mnt/backup_root
```

### Useful software
Archlinux packages to be installed:
- gedit
- gscreenshot
- alsa-utils
- pulseaudio
- waybar
- wlogout
- brightnessctl
- blueberry
- ttf-noto-nerd (music icon in waybar)
- apple-fonts (yay)

## Configure Dracula theme
```bash
# Download Dracula theme and unzip in /usr/share/themes. The folder must be named Dracula
gsettings set org.gnome.desktop.interface gtk-theme "Dracula"
gsettings set org.gnome.desktop.wm.preferences theme "Dracula"


sudo git clone https://github.com/m4thewz/dracula-icons /usr/share/icons/dracula-icons
gsettings set org.gnome.desktop.interface icon-theme "dracula-icons"
```


## XPS 13 (9310)
Information specific to XPS 13 laptop. Tested on XPS 13 9310

### Required packages
Install Sound Open Firmware (sof):
```bash
$ sudo pacman -S sof-firmware
```


