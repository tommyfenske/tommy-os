# tommy-os
A collection of my dotfiles and configs for Linux software

## I use:
Desktop Environment:
- Window Manager: Sway
- Toolbar: Waybar
- Terminal: Alacritty
- Application Launcher: Rofi
- Font: Atkinson Hyperlegible Mono
- Text Editor: Vim
Tools:
- Web Browser: Zen
- IDE: VSCodium
- File Manager: Thunar; nnn
- Notes: Obsidian
- Game Launcher: Lutris
Misc:
- GitHub Desktop
- Audacious
- OBS

## Issues and their fixes:
### Waybar not showing in Sway
When this happened to me, I tried starting Waybar through the terminal.
```
waybar
```
After some time attempting to start, it timed out and I received an error similar to this:
```
[Error] Error calling startservicebyname for org.freedesktop.portal.Desktop
```
I found [this fix](https://github.com/flatpak/xdg-desktop-portal/issues/986#issuecomment-1549698643) by first installing dbus-broker and then running the command:
```
sudo systemctl enable --global dbus-broker.service
```
