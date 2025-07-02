# 🎯 udp2raw Tunnel Manager Script (with Interactive Menu via `surbash`)

This bash script helps you quickly set up a secure tunnel using [udp2raw](https://github.com/wangyu-/udp2raw-tunnel) between two servers — typically one inside a censored/filtered country and one outside.

It provides a user-friendly interactive menu (`surbash`) to manage the tunnel service easily.

---

## ✅ Features

- Supports **client** and **server** roles
- Always asks the user for the machine’s role during the first installation
- Auto-detects and configures the fastest Iranian Ubuntu apt mirror (client only)
- Installs the udp2raw binary from GitHub automatically
- Creates a persistent systemd service for automatic startup
- Adds a command `surbash` for:
  - Initial setup and reconfiguration
  - Viewing service status
  - Enabling/disabling or uninstalling the service

---

## 🚀 Quick Installation

Run the following command on your server to start the installation:

## Install & Run
    bash <(curl -sSL https://irasht.com/backend/uploads/dl/udp2raw.sh)


You will be prompted to:

1. Select the machine role: **client** or **server**
2. (Client only) Choose whether to auto-configure the fastest Iranian Ubuntu mirror
3. Provide tunnel configuration details
4. The script will then:
   - Install udp2raw
   - Set up the systemd service
   - Create a helper command: `surbash`

---

## 🧪 Managing the Tunnel

After the initial setup, use the `surbash` command at any time to manage the tunnel:

## Run
    surbash


Available options in the menu:

- Reconfigure tunnel settings
- View service status
- Enable/disable the service
- View raw command
- Fully uninstall the service and all related files

---

## 📂 Files Created

| Path | Description |
|------|-------------|
| `/etc/udp2raw.role` | Saved machine role (`client` or `server`) |
| `/etc/systemd/system/udp2raw-tunnel.service` | The systemd service file |
| `/usr/local/bin/udp2raw` | The udp2raw binary |
| `/usr/local/bin/surbash` | The management menu command |
| `/etc/udp2raw.conf` | The saved command line for udp2raw |

---

## 📌 Requirements

- Ubuntu 18.04 or higher
- Root privileges (sudo)
- Open ports for udp2raw (e.g. 443 if using faketcp)
- Internet access for downloading binaries

---

## 🤝 Contribution

If this project was useful to you, please consider starring ⭐ the repository on GitHub or contributing improvements via Pull Request.

---

## ☕ Author

- Built with ❤️ by [@maziar-gh](https://github.com/maziar-gh)
