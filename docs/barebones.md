# Barebones

## Installation

### Mirrors selection

Packages are downloaded from [mirror servers](https://wiki.archlinux.org/title/Mirrors).
[Reflector](https://wiki.archlinux.org/title/Reflector) updates the mirror list by 20 most 
recently synchronized HTTPS mirrors and sorting them by download rate after connecting to the
internet on the live system.

The higher a mirror is placed in the list, the more priority it is given when downloading a package.
Usually, the one generated on the live system is fine. If not, it may be [edited](https://wiki.archlinux.org/title/Help:Reading#Append,_add,_create,_edit).


### Essential packages installation

**Optional**: ```base-devel``` , ```vim```

```
pacstrap /mnt base base-devel linux linux-firmware btrfs-progs vim
```


## System configuration

```
 EDITOR=vim visudo
```

### Fstab

```
genfstab -U /mnt >> /mnt/etc/fstab
```

### Chroot

```
arch-chroot /mnt/
```

### TIme-zone

```
ln -sf /usr/share/zoneinfo/Region/City /etc/localtime
```

```
hwclock --systohc
```

### Localization

```
locale-gen
```

### Network configuration

```
/etc/hostname
```

### Initramfs

```
mkinitcpio -P
```

### Password creation

```
passwd
```

### User creation

```
useradd -mG wheel <YOUR-USERNAME>
```

```
%wheel ALL=(ALL) ALL
```

```
%wheel ALL=(ALL) ALL
```

```
passwd <YOUR-USERNAME>
```

```
pacman -S networkmanager
```

```
systemctl enable NetworkManager
```

## Bootloader

### Systemd-boot as bootloader

```
 bootctl --path=/boot install
```

```
 echo blkid -s UUID -o value /dev/sda2 >> /boot/loader/entries/arch.conf
```

```
vim boot/loader/entries/arch.conf 
```

```
vim /boot/loader/loader.conf
```

```
exit
```

```
umount -a
```

## Reboot

```
reboot
```