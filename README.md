# amd64-arm
Set up an emulated Debian 64-bit (amd64) environment on an ARM computer/SBC. Requires Debian or one of its derivatives like Raspberry Pi OS (previously Raspbian).

## Tested hardware

Raspberry Pi 4B

You need to download amd64-arm at https://raw.githubusercontent.com/thetechstoner/amd64-arm/refs/heads/main/amd64-arm and run the below commands in the terminal:

```
# install
chmod +x <path_to_amd64-arm>
sudo <path_to_amd64-arm>

# install (choose debian version)
chmod +x <path_to_amd64-arm>
sudo <path_to_amd64-arm> <debian_codename>

# uninstall
chmod +x <path_to_amd64-arm>
sudo <path_to_amd64-arm> uninstall
```
# usage
amd64 # access chroot terminal

exit # exit chroot terminal

or run amd64.desktop

Menu > Accessories > Terminal (amd64)