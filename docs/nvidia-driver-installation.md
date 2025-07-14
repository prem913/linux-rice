# Nvidia Driver Installation

* [Source](https://github.com/korvahannu/arch-nvidia-drivers-installation-guide)

---

## Initial Steps

```
sudo pacman -Syu
sudo pacman -S base-devel linux-headers git nano --needed
mkdir -p ~/temp
cd ~/temp
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si
```

---

## Enable Multilib Repository

* Uncomment the following lines in the file `vim /etc/pacman.conf`

* ```text
      [multilib]
      Include = /etc/pacman.d/mirrorlist
  ```

* `yay -Syu`

---

## Install Driver Packages

* For Nvidia 1650 `yay -S nvidia-open nvidia-utils lib32-nvidia-utils nvidia-settings`

___

## Enable Driver Modules
