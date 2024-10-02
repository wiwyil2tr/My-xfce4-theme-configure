## XFCE Desktop Beautification Tutorial

### Introduction

This script can quickly configure XFCE desktop, vim, ranger, and zsh to the styles shown in the screenshots, and it allows for easy restoration. It features simplicity and efficiency.

The script also includes some themes and wallpapers.

Currently, this script is only suitable for Arch-based distributions.

It has been optimized for high-resolution displays (1080p and above), adjusting fonts and interface sizes to fit high DPI screens.

- Dependencies: xfce4 (must be installed manually), rofi, picom, lunar-calendar, vala-panel-appmenu-registrar, vala-panel, vala-panel-appmenu-xfce, xfce4-docklike-plugin, xfce-superkey, kdeconnect, copyq, vim (optional, must be installed manually), zsh (optional, must be installed manually), ranger (optional, must be installed manually).

### i3wm Compatibility

This script provides seamless switching between XFCE and i3wm without needing to log out. You can stack, tile, or switch between xfce4-panel and polybar. It should be used with the [i3wm configuration script](https://github.com/wiwyil2tr/My_i3wm_theme_configure). The shortcuts are as follows:

- `Super+Shift+i`: Switch to i3 window manager (press twice to kill polybar and use xfce4-panel).
- `Super+Shift+p`: Kill xfce4-panel.
- `Alt+p`: Enable/restart polybar.
- `Alt+Shift+p`: Kill polybar and enable xfce4-panel.
- `Super+Shift+x`: Switch to xfce4 (original state, i.e., xfce4-panel + xfwm + xfdesktop).

### Notes

- During installation, you can choose to default to a light or dark theme. Both themes will be installed, and you can modify them in XFCE settings afterward.
- Some shortcuts have been modified according to i3's operation style.
- You need to manually change the region in the weather plugin
- This script will not change the default shell; if you are not using zsh, you need to manually use the chsh command to change the default shell.
- XFCE configurations are all copied; vim, ranger, and zsh can be copied or linked.

  - If you choose the copy method, you can delete or move this directory after successful installation. If you choose the link method, do not delete or move this directory after installation.
  - If you choose the link method, make sure to place the directory in your home directory without renaming it; otherwise, it will fail.
- Vim and zsh are optional configurations and can be chosen based on your needs.
- Known issue: The wallpaper configuration may not take effect after installation; you can manually set the wallpaper following the instructions in `Wallpaper.webm`.

### Installation

Run:

```bash
./install.sh
```

After execution, the script will back up the XFCE-related files from the `$HOME/.config` and `$HOME/.local/share` directories to the `My-xfce4-theme-configure/light (or dark)/xfce.ori` directory.

Once the script finishes, please restart your system to use the new theme.

### Restoration

Run:

```bash
./install.sh --restore
```
