# Post-Installation

![Bootloader.png](img/Bootloader.png)

![Enter_passphrase.png](img/Enter_passphrase.png)

![Set_bigger_font_tty.png](img/Set_bigger_font_tty.png)

## Snapshots

```
cd
sudo pacman -Syu
```

![Pacman_syuuuuu.png](img/Pacman_syuuuuu.png)

```
cd Downloads/
sudo pacman -S go
git clone https://aur.archlinux.org/yay.git
cd yay/
makepkg -i
```

![Yay_install.png](img/Yay_install.png)

```
yay -S timeshift
sudo timeshift --create --comments "Testing..."
sudo timeshift --list
```

![Timeshift_testing.png](img/Timeshift_testing.png)

```
sudo pacman -S cowsay
```

![Cowsay_hi](img/Cowsay_hi.png)

```
sudo timeshift --restore
```

![Timeshift_restore](img/Timeshift_restore.png)

```
reboot
```

![Successful_restore](img/Successful_restore.png)

## Graphical User Interface

There it is. A minimal install. For desktop use, it is highly recomended to use a graphical
environment. Choosing one can be a true hassle. For this, virtually any guide suffices 
since this distro is well-known for its ricing community. For now, Archmoured encourages the 
usage of [Xfce](https://wiki.archlinux.org/title/Xfce), for it brings a truly stable 
experience.