# WireGuird GUI for Void Linux

An `.xbps` package for [WireGuird](https://github.com/UnnoTed/wireguird), built from the official source code for Void Linux. 

WireGuird is a Linux GTK GUI client for WireGuard. It lists tunnels from `/etc/wireguard` and controls Wireguard through `wg-quick`.

## Screenshots

| Main Interface | Edit Tunnel |
| :---: | :---: |
| ![Main Interface](Screenshots/main_interface.png) | ![Edit Tunnel](Screenshots/edit_tunnel.png) |

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
