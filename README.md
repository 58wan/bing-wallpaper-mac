# 🖼️ Bing Wallpaper for macOS

Automatically update your macOS wallpaper with Bing's daily image.

## ✨ Features

- 💪 Fix the exception where BIN-DIR is empty during installation.
- 🔄 Auto-updates wallpaper at 11:00 every day. Because only one picture per day.
- 🔍 Add -r random set wallpaper

## 💡 Tips

- During the installation process, I found that the default value must also be entered when setting config.
- Updating every hour is useless because Bing only updates one wallpaper per day. You can set the timing of scheduled tasks in install.sh.
- Add a function to randomly select a downloaded wallpaper, which can manually add fun!

## 🚀 Installation

### Prerequisites

- macOS 10.12 or later
- [jq](https://stedolan.github.io/jq/) (JSON processor)
  
  ```bash
  # Install using Homebrew
  brew install jq
  
  # Or using MacPorts
  sudo port install jq
  ```

### Install

Clone Code:
```bash
git clone https://github.com/58wan/bing-wallpaper-mac.git
```

Simply run the script:

```bash
cd bing-wallpaper-mac
./install.sh
```

## 🗑️ Configuration

The script can be configured using the following commands:

```bash
# Run configuration wizard
bing_wallpaper --config

# View current settings
bing_wallpaper --show-config
```

Configuration options include:
- Resolution (Auto/4K/Full HD/HD)
- Auto-cleanup settings
- Wallpaper save location

## 🗑️ Uninstallation

To remove the app:
```bash
cd bing-wallpaper-mac
./uninstall.sh
```

## 📁 File Structure

- `bing_wallpaper.sh`: Main script for downloading and setting wallpaper
- `~/.wallpapers/`: Directory where wallpapers are stored
- `~/.config/bing-wallpaper/config`: Configuration file
- `~/Library/LaunchAgents/com.${USER}.bingwallpaper.plist`: LaunchAgent configuration

## 📝 Logs

Log files are stored in:
- `~/.wallpapers/bing_wallpaper.out`: Standard output
- `~/.wallpapers/bing_wallpaper.err`: Error messages

## 🤝 Contributing

Feel free to submit issues and enhancement requests!

## 📝 License

MIT License - feel free to use and modify as you like!

