<div align="center">

<img src="https://raw.githubusercontent.com/ez-domain/images/main/logo/ezdomain.png" width="350" alt="ezdomain logo"/>

**Map friendly local domain names to your services with automatic HTTPS**

`project.test → localhost:3000` in seconds, trusted certificate included

[![macOS](https://img.shields.io/badge/macOS-arm64%20%7C%20amd64-black?logo=apple)](https://github.com/ez-domain/install/releases/latest)
[![Linux](https://img.shields.io/badge/Linux-arm64%20%7C%20amd64-orange?logo=linux&logoColor=white)](https://github.com/ez-domain/install/releases/latest)
[![Windows](https://img.shields.io/badge/Windows-x64-blue?logo=windows)](https://github.com/ez-domain/install/releases/latest)
[![Latest Release](https://img.shields.io/github/v/release/ez-domain/install?label=latest&color=brightgreen)](https://github.com/ez-domain/install/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/ez-domain/install/total?label=downloads)](https://github.com/ez-domain/install/releases)

</div>

---

## What is ezdomain?

ezdomain is a background service that gives your local services real domain names and HTTPS. You point a name at a port, and it handles DNS, certificates, and proxying automatically.

```
myapp.test         →  localhost:3000
api.test           →  192.168.1.10:8080
dashboard.test     →  0.0.0.0:4000
```

It manages its own certificate authority and installs it into your system trust store, so browsers treat the certs as valid without any manual steps.

[![Watch the demo](https://img.shields.io/badge/YouTube-Watch%20Demo-red?logo=youtube)](https://youtu.be/jw6Z5H4halM)

---

## Features

- **Automatic HTTPS** — generates a name-constrained local CA, signs per-domain certificates, and installs it into your system trust store.
- **DNS server** — resolves your custom domains on port 53 (LAN) and 5300 (local fallback), with upstream forwarding for everything else. Also works as a DNS-over-HTTPS resolver for Android devices.
- **Reverse proxy** — forwards HTTPS traffic to any local IP:port target, including services that use self-signed certificates.
- **Proxmox integration** `v0.5.0` — apply DNS and CA trust to all VMs and LXC containers directly from the dashboard, with an auto-apply watcher for new guests. Only available when ezdomain is installed on a Proxmox node.
- **Web dashboard** — manage aliases, stream live logs, and configure other devices with one-command DNS setup scripts for macOS, Linux, and Windows.
- **Real-time log viewer** — live log streaming with level filtering and export to `.txt`.
- **Connectivity check** — ping badge on each alias shows whether the target is reachable.
- **In-app updates** `v0.3.0` — update to the latest version directly from the dashboard, no terminal required.
- **Runs as a system service** — starts on boot, managed by the OS service manager.
- **Single binary** — the entire app (UI included) is embedded in one self-contained executable.

---

## Supported Platforms

| OS | Architecture | Installation |
|----|---|---|
| macOS | Apple Silicon (arm64) | `curl` one-liner |
| macOS | Intel (amd64) | `curl` one-liner |
| Linux | amd64 | `curl` one-liner |
| Linux | arm64 | `curl` one-liner |
| Windows | x64 | Setup wizard (`ezdomain-setup.exe`) |

---

## Installation

For full installation instructions, version-specific installs, and scripted options, visit the **[ez-domain/install](https://github.com/ez-domain/install)** repo or download directly from the **[latest release](https://github.com/ez-domain/install/releases/latest)**.

---

## Dashboard

Open **[https://ezdomain.dev](https://ezdomain.dev)** after installation.

| Aliases | Logs | DNS Setup |
|:---:|:---:|:---:|
| <img src="https://raw.githubusercontent.com/ez-domain/images/main/screenshots/Dashboard 1 - Alias Page.png" alt="Alias Page"/> | <img src="https://raw.githubusercontent.com/ez-domain/images/main/screenshots/Dashboard 4 - Logs.png" alt="Log Page"/> | <img src="https://raw.githubusercontent.com/ez-domain/images/main/screenshots/Dashboard 5 - DNS Setup.png" alt="Setup Page"/> |
| DNS Setup 2 | Proxmox DNS (v0.5.0 or above) | Settings |
| <img src="https://raw.githubusercontent.com/ez-domain/images/main/screenshots/Dashboard 6 - DNS Setup 2.png" alt="Alias Page"/> | <img src="https://raw.githubusercontent.com/ez-domain/images/main/screenshots/Dashboard 8 - Proxmox DNS (Proxmox Integration).png" alt="Log Page"/> | <img src="https://raw.githubusercontent.com/ez-domain/images/main/screenshots/Dashboard 7 - Settings.png" alt="Setup Page"/> |

For all screenshots, visit the **[ez-domain/images](https://github.com/ez-domain/images/tree/main/screenshots)** repo.

### Aliases
Add, edit, and delete domain → target mappings. Each alias shows a live ping badge indicating whether the target service is reachable.

### Logs
Live log stream from the ezdomain service with level filtering and one-click export.

### DNS Setup
One-command scripts for macOS, Linux, and Windows — served directly from the dashboard with your host IP pre-filled. Each script auto-detects the network configuration, sets DNS, installs and refreshes the CA certificate, and flushes the cache. A rollback script is provided for each OS.

### Settings
Configure the HTTP listener port (default: `90`). The listener hot-swaps to the new port immediately on save with no service restart. Port 443 for HTTPS is fixed.

---

<div align="center">

Made by [ansori34](https://github.com/ansori34)

</div>
