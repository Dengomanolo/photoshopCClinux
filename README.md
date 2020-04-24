![screenshot](images/Screenshot.png)

![GitHub repo size](https://img.shields.io/github/license/Gictorbit/photoshopCClinux?style=flat) ![Tested on arch](https://img.shields.io/badge/Tested%20on-Archlinux-brightgreen)
![GitHub stars](https://img.shields.io/github/stars/Gictorbit/photoshopCClinux?style=sad) ![rep size](https://img.shields.io/github/repo-size/gictorbit/photoshopCClinux) ![bash](https://img.shields.io/badge/bash-5.0.11-yellowgreen)

# photohop CC v19 installer for linux
This bash script installs Photoshop CC version 19 on your Linux machine using wine behind the scene
and sets some necessary component up for best performance

## Features
* downloads necessary component and installs them (`vcrun`,`atmlib`,`msxml`...)
* downloads photoshop.exe installer and installs it automatically
* creates photoshop commands and desktop entry
* configures wine for dark mode
* detects various graphic cards like (`intel`, `Nvidia`...)
* saves the downloaded files in your cache directory
* It's free and you will not need any license key
* works on any Linux distributions

## Requirements
1- use 64bit edition of your distro

2-make sure below packages are already installed on your Linux distro
* `wine`
* `winetricks`
* `aria2c`
* `md5sum`


if they are not already installed you can install them using your package manager for example in arch Linux
```bash
sudo pacman -Syy wine aria2
``` 
3- make sure you have enogh storage in your `/home` partition about `5 GiB`
> 1 GiB will be free after installation

4- make sure you have internet connection and about 1.5 Gib traffic for downloading photoshop and its components at first time

## Installation
for components installation you have two options, using winetricks or using custom way.
there are two installation scripts

* `PhotoshopSetup.sh`
* `PhotoshopSetupCustom.sh`

installer scripts use a virtual drive of wine and makes a new `winprefix` for photoshop

first of all you need to clone the repository with this command:
```bash
git clone https://github.com/Gictorbit/photoshopCClinux.git
cd photoshopCClinux
```
### component installation using winetricks (Recommended)
for installing photoshop just run the bash script with below command it downloads and installs photoshop include its component using winetricks and configures wine automatically

```bash
chmod +x PhotoshopSetup.sh
./PhotoshopSetup.sh
```

### component installation using custom script
for installing photoshop just run the bash script with below command it downloads and installs photoshop include its component and configures wine automatically

```bash
chmod +x PhotoshopSetupCustom.sh
./PhotoshopSetupCustom.sh
```

during installation please pay attention to script messages

> **NOTE :** make sure OS version in wine is on windows 7

## wineprefix Configuration
if you need to configure wineprefix of photoshop you can use `winecfg.sh` script just run below command
```bash
chmod +x winecfg.sh
./winecfg.sh
```

## Uninstall
for uninstall photoshop you can use uninstaller script with below commands
```bash
chmod +x uninstaller.sh
./uninstaller.sh
```


## License
![GitHub](https://img.shields.io/github/license/Gictorbit/photoshopCClinux?style=for-the-badge)
