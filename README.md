# amd64-arm
Set up an emulated Debian 64-bit (amd64) environment on an ARM computer/SBC. Requires Debian or one of its derivatives like Raspberry Pi OS (previously Raspbian).

## Tested derivatives of Debian on which amd64-arm can be set up

1. Raspberry Pi OS (previously Raspbian)
2. Ubuntu Server

## Tested hardware

1. Raspberry Pi 4B

You need to download amd64-arm at https://raw.githubusercontent.com/thetechstoner/amd64-arm/refs/heads/main/amd64-arm and run the below commands in the terminal:

```
chmod +x <FULL_PATH_TO_DOWNLOADED_FILE>
sudo <FULL_PATH_TO_DOWNLOADED_FILE>
or
sudo <FULL_PATH_TO_DOWNLOADED_FILE> <debian_version_codename>
```
# usage
amd64 # access chroot environment
exit # exit chroot environment
or run amd64.desktop
