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


## XPS 13 (9310)
Information specific to XPS 13 laptop. Tested on XPS 13 9310

### Required packages
Install Sound Open Firmware (sof):
```bash
$ sudo pacman -S sof-firmware
```


