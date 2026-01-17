# Useful Linux commands for CachyOS (& other Arch based systems)

## Boot order & timeout (systemd-boot)

`/boot/loader/loader.conf` - change timeout to 0 (default is 5)

## Cachy specific aliases

Located at `usr/share/cachyos-fish-config/cahyos-config.fish`

**`update`** = sudo pacman -Syu

**`cleanup`** = sudo pacman -Rns (pacman -Qtdq)

## Pacman

Capital Letter for the main operation followed by lowercase letters as flags

`sudo pacman -Syu` - "Universal Update"

- **S** - Sync
- **y** - refresh, updates package list
- **u** - upgrade

### Install

`sudo pacman -S <package>`

### Uninstall

`sudo pacman -Rns <package>` - recommended

- **R** - remove
- **n** - nosave: remove configuration files
- **s** - recursive: remove dependencies that were only needed for this app

`sudo pacman -R <package>` - basic

### Search

`pacman -Ss <keyword>` - search online repo

`pacman -Qs <keyword>` - search installed apps

`pacman -Qi <package>` - shows detailed info about an installed app

### Maintenance

`pacman -Qdtq`
- **Q** - query installed packages
- **t** - show orphans
- **d** - restrict to dependencies
- **q** - quiet output (package names only)

`sudo pacman -Sc` - cleans the "cache"
