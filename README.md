# Hyprland + Omarchy Dual-Monitor Setup 🖥️🖥️

A clean dual-monitor configuration using:
- [Hyprland](https://github.com/hyprwm/Hyprland)
- [Omarchy](https://github.com/omarchy/omarchy)
- [split-monitor-workspaces](https://github.com/Duckonaut/split-monitor-workspaces)
- [Waybar](https://github.com/Alexays/Waybar)

This setup gives **separate workspaces per monitor**, **individual Waybars**, and **custom keybinds** for moving windows between screens.

---

## ✨ Features

✅ 5 workspaces per monitor  
✅ Seamless window movement (Super+Alt or Super+Alt+Shift)  
✅ Independent Waybars with clean numbering  
✅ Works out of the box with Omarchy’s config layering

---

## 📁 Config Overview

### `~/.config/hypr/plugins.conf`
```ini
plugin:split-monitor-workspaces {
    enable = true
    focus_on_switch = false
    count = 5

    map = DP-1, 1 2 3 4 5
    map = DP-3, 6 7 8 9 10
}
```
Ensure to replace dp-1 and dp-3 with actual monitor names. also in waybar-1 and waybar-2
 
## ⌨️ Keybindings
```
# Move focused window to second monitor (6–10)
bind = SUPER_ALT, 1, movetoworkspace, 6
bind = SUPER_ALT, 2, movetoworkspace, 7
bind = SUPER_ALT, 3, movetoworkspace, 8
bind = SUPER_ALT, 4, movetoworkspace, 9
bind = SUPER_ALT, 5, movetoworkspace, 10

# Move within second monitor (6–10)
bind = SUPER_ALT_SHIFT, 1, movetoworkspace, 6
bind = SUPER_ALT_SHIFT, 2, movetoworkspace, 7
bind = SUPER_ALT_SHIFT, 3, movetoworkspace, 8
bind = SUPER_ALT_SHIFT, 4, movetoworkspace, 9
bind = SUPER_ALT_SHIFT, 5, movetoworkspace, 10

```
## 🖼️ Screenshots
![screenshot](./screenshots/monitor_1.png)

![screenshot](./screenshots/monitor_2.png)