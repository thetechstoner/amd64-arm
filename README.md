# amd64-arm
Setup emulated Debian 64-bit (amd64) environment on ARM computer/SBC. Requires Debian-based host system like Raspberry Pi OS.

## Tested hardware

Raspberry Pi 4B

download amd64-arm:
```
curl -LO https://raw.githubusercontent.com/thetechstoner/amd64-arm/main/amd64-arm
```
setup command options in terminal:
```
# install debian bookworm
chmod +x <path_to_amd64-arm>
sudo bash <path_to_amd64-arm>

# install (choose debian version)
chmod +x <path_to_amd64-arm>
sudo bash <path_to_amd64-arm> <debian_codename>

# uninstall
chmod +x <path_to_amd64-arm>
sudo bash <path_to_amd64-arm> uninstall

# schroot environment install .deb file
chmod +x <path_to_amd64-arm>
bash <path_to_amd64-arm> install-deb <path_to_deb_file>

# schroot environment uninstall .deb file
chmod +x <path_to_amd64-arm>
bash <path_to_amd64-arm> uninstall-deb <path_to_deb_file>
```

usage:
```
# access chroot terminal (root)
amd64

# chroot terminal as root
schroot -c amd64 -u root -d /home

# chroot terminal as user
schroot -c amd64 -u $USER -d /home

# exit chroot terminal
exit

# run amd64.desktop
Menu > Accessories > Terminal (amd64)
```
run win64 and Win32 applications on arm64 Linux
https://github.com/AndreRH/hangover