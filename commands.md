# Useful Linux commnds for CachyOS (& other Arch based systems)

Boot order & timeout (systemd-boot)

`/boot/loader/loader.conf` - change timeout 0

## Pacman

Capital Letter for the main operation followed by lowercase letters as flags

`sudo pacman -Syu` - "Universal Update"

- **S** - Sync
- **y** - refresh, updates package list
- **u** - upgrade

### Install

`sudo pacman -S <package>`

### Uninstall

`sudo pacman -R <package>` - basic

`sudo pacman -Rns <package>` - recommended

- **n** (nosave): removes configuration files

- **s** (recursive): removes dependencies that were only needed for this app

### Search

`pacman -Ss <keyword>` - searches online repo

`pacman -Qs <keyword>` - searches _installed_ apps

`pacman -Qi <package>` - shows detailed info about an installed app

### Maintenance

`pacman -Qdt` - list orphans

`sudo pacman -Sc` - cleans the "cache"
