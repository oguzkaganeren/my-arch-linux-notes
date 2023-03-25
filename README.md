# my-arch-linux-notes

## Installation Notes
#### Connect wifi
```iwctl```
Then
```station wlan0 connect SSID```
Then 
```exit```
#### Easy installation
```archinstall```

## After installation
### Yay
```sudo pacman -S --needed git base-devel && git clone https://aur.archlinux.org/yay.git && cd yay && makepkg -si```

### Other packages

```sudo pacman -S aria2 speedtest-cli telegram-desktop kdenlive inkscape virtualbox fish flameshot neofetch gtop kolourpaint gedit autoconf binutils make gcc pkg-config fakeroot libtool automake patch dbeaver tilix x11-ssh-askpass drawing opera chromium spotify-launcher sof-firmware```

```yay -S vscodium-bin mailspring```

### Fish shell
```
chsh -s /usr/bin/fish
curl -L https://get.oh-my.fish | fish
omf install https://github.com/simnalamburt/shellder
```

### Settings

```sudo systemctl enable fstrim.timer```

### Auto mount other partitions
If you have other partitions(E, D etc.). It can be mounted on the startup.

```
lsblk -f
```
The command shows your disks uuid.
```
sudo gedit /etc/fstab 
```
Open your fstab config with the command. You should add codes similar to the following example. You should change UUID and /run/media/yourUserName/Partition.
```
UUID=b336b98e-d0b5-4254-b6aa-9e66f85b0dfc /run/media/oguz/Files ext4 defaults  0 0
```
