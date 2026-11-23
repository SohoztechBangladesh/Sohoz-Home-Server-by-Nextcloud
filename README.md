# ☁️ Sohoz Home Server by Nextcloud

[![Release](https://img.shields.io/badge/Release-v1.0.5-blue.svg)](https://github.com/SohoztechBangladesh/Sohoz-Home-Server-by-Nextcloud/releases/latest)
[![Platform](https://img.shields.io/badge/Platform-Windows%2010%20%7C%2011%20x64-0078D6.svg)](https://github.com/SohoztechBangladesh/Sohoz-Home-Server-by-Nextcloud/releases/latest)
[![Architecture](https://img.shields.io/badge/Architecture-Native%20x64%20(No%20Docker%20%2F%20No%20WSL)-brightgreen.svg)](https://github.com/SohoztechBangladesh/Sohoz-Home-Server-by-Nextcloud/releases/latest)
[![License](https://img.shields.io/badge/License-Commercial%20%2F%20Proprietary-orange.svg)](LICENSE.txt)

> **The Private, Native Windows Alternative to Google Drive, Microsoft OneDrive & Apple iCloud.**  
> High-performance personal cloud storage server engineered natively for 64-bit Windows systems. Zero monthly subscription fees, 100% data sovereignty, and automated mobile camera sync.

---

## 📥 Download Latest Release

Get the standalone 1-click Windows installer from our official GitHub Releases:

👉 **[Download NextcloudServerSetup-v1.0.5-x64.exe](https://github.com/SohoztechBangladesh/Sohoz-Home-Server-by-Nextcloud/releases/latest)** *(v1.0.5 Standalone Setup Wizard)*

| File | Size | Architecture | Checksum (SHA-256) |
| :--- | :--- | :--- | :--- |
| `NextcloudServerSetup-v1.0.5-x64.exe` | ~531 MB | Windows 10 / 11 (64-bit) | `DB0B7289FB848CC0145B060BD26C260EA29A4B25D76EBEDD4B6D6AEBF82A2016` |

---

## 🆕 What's New in v1.0.5

* **Cloudflare Zero Trust & Nginx Firewall Automation:** Added complete automatic inbound and outbound Windows Defender Firewall rules for **Cloudflare Tunnel (`cloudflared.exe`)**, **Nginx (`nginx.exe`)**, **PHP FastCGI (`php-cgi.exe`)**, **PHP CLI (`php.exe`)**, and **HTTP Port 8080** across both Private and Public network profiles (`profile=any`). Completely eliminates the interactive *"Windows Security: Windows Firewall has blocked some features of cloudflared / nginx"* security prompt on Windows 10 and 11.
* **Full-Stack Firewall Lifecycle Integration:** Automated rule creation on setup, automatic cleanup in Uninstaller (`Uninstall.exe` and `Uninstall.cmd`), and proactive silent validation prior to spawning cloudflared or Nginx in the server manager runtime.
* **Streamlined Setup Elevation:** Refined installer UAC self-elevation ensuring all networking configurations, firewall permissions, desktop shortcuts, and autostart registry items install seamlessly with zero privilege friction.
* **Antigravity Diagnostics Cleanup:** Zero warnings, zero unused variables, and 100% clean compilation across all build, packaging, and runtime scripts.

---

## 🆕 What's New in v1.0.4

* **Automated Windows Defender Firewall Configuration:** Integrated seamless automatic firewall rule configuration during setup. Inbound rules are automatically registered for Nginx (`nginx.exe`), HTTP port `8080`, and the Server Controller on both Private and Public network profiles (`profile=any`).
* **Administrator Elevation for Setup:** Enhanced the installer (`InstallerProgram.cs`) with standard UAC elevation so that all system components, firewall rules, and startup items install reliably with full administrative permissions.
* **Clean Firewall Rule Uninstallation:** Uninstaller (`Uninstall.exe` and `Uninstall.cmd`) automatically purges all created firewall rules upon removal.

---

## 🆕 What's New in v1.0.3

* **Cloudflare Tunnel Mobile OAuth Fix:** Fixed mixed-content form submission blocking on iOS Safari and mobile webviews by dynamically resolving trusted proxy HTTPS headers (`X-Forwarded-Proto` and `HTTPS on`) in Nginx. The "Grant access" authorization button now completes pairing immediately.
* **Atomic Super Administrator Update:** Fixed an issue where changing the Super Administrator username and password simultaneously skipped the password update. Both username and password now update atomically within a unified SQLite transaction.
* **Password Visibility in UI:** Added password visibility controls across the Server Manager UI. Administrators can toggle plain-text visibility for both the Super Administrator and configured users using dedicated **👁 Show / Hide Passwords** buttons.

---

## 🌟 Key Highlights

* **100% Physical Data Ownership:** All your photos, family videos, and private documents reside exclusively on your local computer and hard drives—never scanned, mined, or stored by corporate third parties.
* **No Recurring Monthly Subscriptions:** Free yourself from recurring cloud storage fees. Buy a lifetime license once and keep your storage indefinitely.
* **Unlimited Storage Expansion:** Expand your personal cloud at any time. Connect external USB drives or add internal hard drives with 1-click drive mounting.
* **Automated Mobile Camera Roll Backup:** Official Nextcloud iOS and Android app support with instant background photo & video synchronization.
* **Universal In-Browser Viewer (200+ Formats):** Preview Word, Excel, PowerPoint, PDF, CAD/AutoCAD (`.dwg`, `.dxf`), 3D models (`.obj`, `.stl`, `.gltf`), 4K ProRes videos, RAW photos, Markdown, and source code directly in your browser.
* **Encrypted Remote Access (Cloudflare Zero Trust):** Access your home server securely from anywhere in the world over encrypted Cloudflare tunnels with zero router port forwarding and no static IP requirement.
* **Zero Overhead Native Architecture:** Runs directly as optimized Windows 64-bit background services—no WSL2, no Docker, and no virtualization required.

---

## 💻 System Requirements

| Component | Minimum Specification | Recommended Specification |
| :--- | :--- | :--- |
| **Operating System** | Windows 10 (64-bit, Version 1909+) | Windows 11 / Windows 10 Pro (64-bit) |
| **Processor** | Dual-Core 64-bit Intel / AMD x64 | Quad-Core 2.0 GHz or higher |
| **Memory (RAM)** | 4 GB | 8 GB or higher |
| **Disk Space** | 2 GB for installation | Dedicated SSD/HDD for personal cloud storage |
| **File System** | NTFS | NTFS |
| **Network** | Local Wi-Fi or Ethernet LAN | Gigabit Ethernet for maximum local sync speed |

---

## 🚀 Quick Start & Installation

1. **Download:** Download `NextcloudServerSetup-v1.0.5-x64.exe` from the [Releases](https://github.com/SohoztechBangladesh/Sohoz-Home-Server-by-Nextcloud/releases/latest) section.
2. **Install:** Run the installer as Administrator. Select your desired installation directory (Default: `C:\Program Files\Sohoz Nextcloud Server`).
3. **Launch:** Click **Install Now**. Once extraction is complete, launch the server from the Desktop shortcut.
4. **Dashboard:** Access the local management dashboard via system tray or browser at `http://localhost:8080`.
5. **Connect Phones:** Install the official Nextcloud app from Google Play Store or Apple App Store, scan your server QR code, and toggle **Auto Upload** for camera sync.

For complete deployment details, refer to the [USER_MANUAL.txt](USER_MANUAL.txt).

---

## 🔑 Licensing & Software Activation

**Sohoz Home Server by Nextcloud** is proprietary software distributed as a closed-source solution. The Windows desktop orchestration supervisor, system tray controller, drive mounter, and hardware-bound license engine are proprietary software developed by **Rakib Mollah** and published by **Sohoztech Software Solutions Bangladesh**.

To unlock full lifetime operation on your machine, a hardware-bound license key is required.

### How to Obtain an Activation License:
To acquire a valid lifetime license key for your device:

* **Lead Developer:** Rakib Mollah
* **Organization:** Sohoztech Software Solutions Bangladesh
* **Official Email:** [sohoztech.business@gmail.com](mailto:sohoztech.business@gmail.com)
* **WhatsApp Support:** `+8801927432612`
* **Facebook Page:** [Sohoztech Software Solutions](https://www.facebook.com/share/1CWVuNKVem/?mibextid=wwXIfr)

---

## ⚖️ Legal & GitHub Terms of Service Compliance

* **Dual-Licensing Structure:** The core server engine utilizes Nextcloud Server Core licensed under the GNU Affero General Public License Version 3 (GNU AGPLv3). In strict compliance with AGPLv3, Nextcloud core source files and license notices remain accessible.
* **Proprietary Components:** The Windows Controller suite, setup installer, background supervisor, and drive orchestration tools are proprietary commercial works owned by Rakib Mollah / Sohoztech Software Solutions Bangladesh.
* **Security & Distribution Policy:** In compliance with GitHub Acceptable Use Policies and Terms of Service, this public repository contains exclusively verified, official release assets and public documentation. No internal key generators, private signing tools, or security bypass mechanisms are hosted in this public repository.
* **Trademarks:** Nextcloud is a registered trademark of Nextcloud GmbH. Google Drive, Microsoft OneDrive, and Apple iCloud are trademarks of their respective owners. Sohoz Home Server is an independent solution and is not affiliated with or endorsed by these entities.
