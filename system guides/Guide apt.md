# Zsh Guide

## Updating Packages
```zsh
sudo apt update
sudo apt upgrade
```
If no issue: 
```zsh
reboot
```

### Cleaning
Monthly
```zsh
sudo apt autoremove --purge
sudo apt autoclean
```


### Trouble shooting - missing key
Only run if missing key error (e.g. "GPG error" or "NO_PUBKEY")
```zsh
sudo apt update
sudo apt install kali-archive-keyring
```

### Trouble shooting - clear boot space:
Only run if boot space error.

1- list existing kernels and print current kernel (this one should NOT be deleted)
```zsh
dpkg --list | grep linux-image
uname -r
```
2- manually delete oldest kernel
```zsh
sudo apt purge linux-image-x.x.x-x
sudo apt autoremove --purge
```

### Trouble shooting - packages held back 
More aggressive than upgrade: this can remove old packages to resolve dependencies
```zsh
sudo apt full-upgrade
```


## Search past commands
List history when COMMAND appears - note the command number
```zsh
history | grep COMMAND
```

Copy the corresponding row to terminal (doesn't run it)
```zsh
!COMMAND_NUMBER
```
