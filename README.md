## userconf-pi

Rename a user for HamoniKR arm64

 * upstream : https://github.com/RPi-Distro/userconf-pi

### Changes
 * Change rpi-first-boot-wizard user env to zsh

## tips
Create a file named user userconf (or userconf.txt) containing the following:
```
pi:$6$c70VpvPsVNCG0YR5$l5vWWLsLko9Kj65gcQ8qvMkuOoRkEagI90qi3F/Y7rm8eNYZHW8CY6BOIKwMH7a3YYzZYL90zf304cAHLFaZE0
```
Place userconf (or userconf.txt) plus an empty file named ssh (or ssh.txt) in the BOOT (FAT32) partition of the SD card.
Insert the SD card in the Raspberry Pi and it should boot with access to user 'pi' (password : raspberry) via SSH.

### options for raspi-config

`sudo raspi-config nonint do_boot_behaviour B4`

B1: Boot to console, requiring login.
B2: Boot to console, logging in automatically (this is what the command you provided does).
B3: Boot to desktop, requiring login.
B4: Boot to desktop, logging in automatically.