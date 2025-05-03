# amd64-arm
Setup emulated Debian 64-bit (amd64) environment on ARM computer/SBC. Requires Debian-based host system like Raspberry Pi OS.

## Tested hardware

Raspberry Pi 4B

download amd64-arm at https://raw.githubusercontent.com/thetechstoner/amd64-arm/refs/heads/main/amd64-arm

run below commands in terminal:

```
# install debian bookworm
chmod +x <path_to_amd64-arm>
sudo <path_to_amd64-arm>

# install (choose debian version)
chmod +x <path_to_amd64-arm>
sudo <path_to_amd64-arm> <debian_codename>

# install .deb file in chroot environment
chmod +x <path_to_amd64-arm>
sudo <path_to_amd64-arm> install-deb <path_to_deb_file>

# uninstall .deb file in chroot environment
chmod +x <path_to_amd64-arm>
sudo <path_to_amd64-arm> uninstall-deb <path_to_deb_file>

# uninstall
chmod +x <path_to_amd64-arm>
sudo <path_to_amd64-arm> uninstall
```
# usage
'''
# access chroot terminal (root)
amd64

# exit chroot terminal
exit

# chroot terminal as root
schroot -c amd64 -u root -d /home

# chroot terminal as user
schroot -c amd64 -u $USER -d /home

run amd64.desktop

Menu > Accessories > Terminal (amd64)
'''
run win64 and Win32 applications on arm64 Linux
https://github.com/AndreRH/hangover