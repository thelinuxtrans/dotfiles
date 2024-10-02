install.sh:

```
#!/bin/bash

# Welcome message
echo "Hello and Welcome to TheLinuxTrans' Hyprland install wizard."

# Define base directory for installation (customize as needed)
BASE_DIR="$HOME/.config/TheLinuxTransHyprland"

# Create necessary directories
declare -a FOLDERS=(
    "BetterDiscord"
    "byobu"
    "cava"
    "Code"
    "Code-OSS"
    "dconf"
    "discord"
    "Discord"
    "Electron"
    "firefox"
    "gh"
    "GIMP"
    "go"
    "gtk-3.0"
    "htop"
    "hypr"
    "kde.org"
    "kitty"
    "mako"
    "neofetch"
    "obs-studio"
    "pulse"
    "ranger"
    "rofi"
    "session"
    "spicetify"
    "spotify"
    "systemd"
    "Thunar"
    "Vencord"
    "viewnior"
    "wal"
    "waybar"
    "xfce4"
)

# Create folders
for folder in "${FOLDERS[@]}"; do
    mkdir -p "$BASE_DIR/$folder"
done

# Define files to copy (customize the source paths as needed)
declare -a FILES=(
    "dolphinrc"
    "kritadisplayrc"
    "kritarc"
    "pavucontrol.ini"
    "user-dirs.dirs"
    "user-dirs.locale"
)

# Copy files (customize the source paths as needed)
for file in "${FILES[@]}"; do
    if [[ -f "$HOME/$file" ]]; then
        cp "$HOME/$file" "$BASE_DIR/$file"
        echo "Copied $file to $BASE_DIR."
    else
        echo "$file does not exist in $HOME. Skipping."
    fi
done

echo "Installation complete! Your Hyprland setup is ready."

```
