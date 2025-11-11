# Troubleshoot your Archlinux system

## Not booting
If the system is fucked because of a bad update of wrong parameter is some config, you can always get access to a working shell by booting from a LIVE ISO.

### Mount the disk
```bash
$ loadkeys <LANG>
$ # Decrypt disk
$ cryptsetup luksOpen /dev/nvme0n1p2 <LUKS_ALIAS>

$ # Mount disks
$ mkdir /mnt/disk
$ mount /dev/<LVM_DISK>/<ROOT_PARTITION> /mnt/disk
$ mount /dev/<LVM_DISK>/<HOME_PARTITION> /mnt/disk/home
```

### Use pacman from live iso to re-install software 
```bash
$ pacman -S <PACKAGE_TO_INSTALL> --root /mnt/disk
```

### chroot in the disk

```bash
$ arch-chroot /mnt/disk
```

