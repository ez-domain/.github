<div align="center">

<img src="https://raw.githubusercontent.com/ez-domain/images/main/logo/ezdomain.png" width="350" alt="ezdomain logo"/>

**Map friendly local domain names to your services with automatic HTTPS**

`project.test → localhost:3000` in seconds, trusted certificate included

[![macOS](https://img.shields.io/badge/macOS-arm64%20%7C%20amd64-black?logo=apple)](https://github.com/ez-domain/install/releases/latest)
[![Linux](https://img.shields.io/badge/Linux-arm64%20%7C%20amd64-orange?logo=linux&logoColor=white)](https://github.com/ez-domain/install/releases/latest)
[![Windows](https://img.shields.io/badge/Windows-x64-blue?logo=windows)](https://github.com/ez-domain/install/releases/latest)

</div>

---

## What is ezdomain?

ezdomain is a lightweight local domain manager that lets you access your development services through clean, memorable `.test` (or any TLD) domain names — served over **HTTPS with a fully trusted local certificate**.

No more `localhost:3000`. Just `myapp.test`.

```
myapp.test         →  localhost:3000
api.test           →  192.168.1.10:8080
dashboard.test     →  0.0.0.0:4000
```

It runs as a background service on your machine, handles DNS resolution, manages a local certificate authority, and reverse-proxies all HTTPS traffic automatically.

---

## Features

- **Automatic HTTPS** — generates a local CA, signs per-domain certificates, and installs it into your system trust store. No browser warnings.
- **DNS server** — resolves your custom domains on port 53 (LAN) and 5300 (local fallback), with upstream forwarding for everything else.
- **Reverse proxy** — forwards HTTPS traffic to any local IP:port target.
- **Web dashboard** — manage aliases, stream live logs, and get DNS setup instructions for other devices on your network.
- **Real-time log viewer** — live log streaming with level filtering (INFO / WARN / ERROR / DEBUG) and export to `.txt`.
- **Connectivity check** — ping badge on each alias shows whether the target is reachable.
- **Runs as a system service** — starts on boot, managed by the OS service manager (launchd / systemd / Windows SCM).
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

For full installation instructions, version-specific installs, and scripted options — visit the **[ez-domain/install](https://github.com/ez-domain/install)** repo or download directly from the **[latest release](https://github.com/ez-domain/install/releases/latest)**.

---

## Dashboard

Open **[https://ezdomain.dev](https://ezdomain.dev)** after installation.

<img src="https://raw.githubusercontent.com/ez-domain/images/main/screenshot/dashboard-1.png" width="700" alt="ezdomain dashboard"/>

### Aliases
Add, edit, and delete domain → target mappings. Each alias shows a live ping badge indicating whether the target service is reachable.

### Logs
Live log stream from the ezdomain service with level filtering and one-click export.

### Setup
Instructions to point other devices on your LAN to your machine's DNS — so your custom domains work across your entire local network.

---

<div align="center">

Made by [ansori34](https://github.com/ansori34)

</div>
