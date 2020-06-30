# My custom st build

## Patches
* alpha
* anysize
* bold is not bright
* hidecursor
* scrollback

## Install
```sh
git clone https://gitlab.com/CamelCoder/st
cd st
sudo make clean install
```

## Color Emoji support
For color emoji support install libxft with the bgra patch.

### On Arch based systems
```sh
git clone https://aur.archlinux.org/libxft-bgra.git
cd libxft-bgra
# Libxft-bgra isn't properly packaged, its therefore needed to replace the architecture manually.
# This can be done by replacing <<ARCH>> with your architecture and runnung the following command:
# sed -i "s/x86_64/<<ARCH>>/g" PKGBUILD
makepkg -si
```

### Other
```sh
git clone --depth=1 https://gitlab.com/zanc/xft
cd xft && ./configure && sudo make instal
sudo ldconfig && reboot
```

## Documentation / Keybinds
```sh
man st
```
