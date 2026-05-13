# Secure Vault Guide
- 3 copies (desktop, laptop, USB)
- 2 media types (SSD/HDD + USB stick)
- 1 offsite (GitHub, technically)

## Update Crytomator (regularly, but not urgently!)
```zsh
flatpak update
```

## Git pull
```zsh
cd ~/Documents/perso/secure_vault
git pull 
```
## Unlock Vault
```zsh
flatpak run org.cryptomator.Cryptomator
```
Press Unlock and input password.
## Use Vault
Once opened, you can use the decrypted folder at:
```zsh
cd ~/.local/share/Cryptomator/mnt/secure_vault
```
## Lock Vault
Press Lock once finished. 

## Git push
```zsh
cd ~/Documents/perso/secure_vault
git add .
git commit -m "commit message"
git status
git push 
```

## Save data to usb key (once a year)
check where the usb is mounted (typically /run/media/lucien/KINGSTON)
```zsh
df -h | grep KINGSTON
```
then copy paste in usb key
```zsh
mkdir -p /run/media/lucien/KINGSTON/save_XXX
rsync -ah --info=progress2 ~/Documents/perso/secure_vault/ /run/media/lucien/KINGSTON/save_XXX/secure_vault/
```

## First time setup (new device)
Install flatpak
```zsh
sudo apt install flatpak
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
flatpak install flathub org.cryptomator.Cryptomator
```
Set up github
```zsh
cd ~/Documents/perso
sudo apt install gh
gh auth login
gh repo clone lpc49/secure_vault
```
Set up Cryptomator
```zsh
flatpak run org.cryptomator.Cryptomator
```
-> open existing vault -> navigate to vault.cryptomator -> unlock now

