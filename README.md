# WireGuird GUI for Void Linux

An `.xbps` package for [WireGuird](https://github.com/UnnoTed/wireguird), built from the official source code for Void Linux. 

WireGuird is a Linux GTK GUI client for WireGuard. It lists tunnels from `/etc/wireguard` and controls Wireguard through `wg-quick`.

## Screenshots

| Main Interface | Edit Tunnel |
| :---: | :---: |
| ![Main Interface](Screenshots/main_interface.jpg) | ![Edit Tunnel](Screenshots/edit_tunnel.jpg) |

## Package Details
* **Version:** 1.1.0
* **Tested Environment:** Void Linux with **Xfce** desktop environment (System tray/AppIndicator required).
* **Original Source:** [UnnoTed/wireguird](https://github.com/UnnoTed/wireguird)
* **License:** MIT

## Installation

1. Download the `.xbps` file from the [Releases](../../releases) page.
2. Install the package locally using the following command (replace the path with your actual download path):
   ```bash
   sudo xbps-install -R /path/to/downloaded/file wireguird

## Build from Source (Void Linux)

If you prefer to build the package yourself using `xbps-src`, follow these steps:

1. Clone the `void-packages` repository and set it up:
   ```bash
   git clone --depth 1 https://github.com/void-linux/void-packages.git
   cd void-packages
   ./xbps-src binary-bootstrap
2. Create the package directory and add the template:
   ```bash
   mkdir -p srcpkgs/wireguird
3. Copy the template file provided in this repository to the newly created directory:
   ```bash
   cp /path/to/this/repository/template srcpkgs/wireguird/template
4. Build the package:
   ```bash
   ./xbps-src pkg wireguird
5. Install your newly built package:
   ```bash
   sudo xbps-install --repository=hostdir/binpkgs -f wireguird

## Start automatically on login (XFCE)
   
1. Ensure the autostart directory exists:
   ```bash
   mkdir -p ~/.config/autostart
2. Create a configuration file:
   ```bash  
   nano ~/.config/autostart/wireguird.desktop
3. Populate the file details and save:
   ```bash
   [Desktop Entry]
   Encoding=UTF-8
   Version=1.1
   Type=Application
   Terminal=false
   Exec=sh -c "sleep 5 && pkexec /opt/wireguird/wireguird"
   Name=Wireguird
   Icon=/opt/wireguird/Icon/128x128/wireguard.png
   Categories=Network;Application;
   X-GNOME-Autostart-enabled=true
   StartupNotify=false
4. Make it actionable:
   ```bash
   chmod +x ~/.config/autostart/wireguird.desktop
