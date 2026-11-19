# LambdaOS-repo

Signed pacman packages for **LambdaOS**, a personal Arch Linux setup: Hyprland + the HEV Quickshell desktop.
The packages are in the [`x86_64` release](https://github.com/DCapps1994/LambdaOS-repo/releases/tag/x86_64).
This repo holds no source code.

LambdaOS is a non-commercial fan project. It is not made, endorsed or supported by Valve.

## Use it on Arch Linux

1. Trust the signing key:
   ```sh
   sudo pacman-key --recv-keys 36AA2BC9D25AA07F564BC8166547BC1A4686B300 --keyserver keyserver.ubuntu.com
   # or, without a keyserver:
   curl -L https://github.com/DCapps1994/LambdaOS-repo/releases/download/x86_64/lambda-keyring-key.gpg | sudo pacman-key --add -
   sudo pacman-key --lsign-key 36AA2BC9D25AA07F564BC8166547BC1A4686B300
   ```
2. Add the repo to `/etc/pacman.conf`:
   ```ini
   [lambda]
   Server = https://github.com/DCapps1994/LambdaOS-repo/releases/download/x86_64
   ```
3. `sudo pacman -Syu lambda-keyring`. After that the keyring package keeps the key up to date.

Key fingerprint: `36AA 2BC9 D25A A07F 564B  C816 6547 BC1A 4686 B300` (LambdaOS Repo Signing, ed25519).

## Packages
| Package | What |
|---|---|
| `hev` | the desktop shell |
| `lambda-system` | system configuration (login screen, services, os-release) |
| `lambda-keyring` | the signing key |
| `lambda-meta` | the full desktop |
| `lambda-apps` | optional app set |
| others | rebuilds of AUR packages the desktop uses |
