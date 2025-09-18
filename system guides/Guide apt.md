# Zsh Guide

## Updating Packages

```zsh
sudo apt update
sudo apt upgrade
sudo apt autoremove
reboot
```

if needed: manually download and install the new archive signing key:
```zsh
sudo wget https://archive.kali.org/archive-keyring.gpg -O /usr/share/keyrings/kali-archive-keyring.gpg
```

if needed: clear boot space:
1- print current kernel and list existing kernels.
```zsh
uname -r
dpkg --list | grep linux-image
```
2- delete oldest kernel
```zsh
sudo apt purge linux-image-x.x.x-x
```


## Search past commands
```zsh
history | grep COMMAND
!COMMAND_NUMBER
```
