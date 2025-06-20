# amd64-arm
Setup emulated schroot Debian 64-bit (amd64) environment on ARM computer/SBC. Requires Debian-based host system like Raspberry Pi OS.
```
user-mode emulation (schroot/chroot/proot)
Emulation: User-mode (qemu-x86_64-static)
Filesystem: Direct host bind mounts
Networking: Shared host network stack
Performance: Moderate (CPU emulation)
Security: Potential breakout risks
should not be relied upon for containing untrusted code

schroot will not work for complex apps
chromium/electron based apps wont work
Terminal based programs only

to run more apps use:
kvm-hosted mode (qemu handles device emulation and kvm accelerates cpu execution)
Emulation: Full system emulation with KVM
Filesystem: Isolated virtual disk
Networking: Virtual bridge (virbr0)
Performance: Near-native (hardware virt)
Security: Strong process isolation
```
## Tested hardware

Raspberry Pi 4B

download amd64-arm:
```
curl -LO https://raw.githubusercontent.com/thetechstoner/amd64-arm/main/amd64-arm
```
schroot setup command options in terminal:
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

# schroot environment integrate desktop and icon files in system (remove unused files)
chmod +x <path_to_amd64-arm>
bash <path_to_amd64-arm> integrate-system
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