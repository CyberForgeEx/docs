# PowerBash  
**Cross-Platform System Administration Toolkit (PowerShell + Bash)**

The ultimate unified sysadmin utility that works **identically** on **Windows** and **Linux** one menu, one experience, zero learning curve. Kill processes, monitor health, check disk space, hash files, geolocate IPs, view network stats, create timestamped backups all with beautiful color output and full logging.

Current Version: **1.0.0** • Windows 10/11 + Linux (Ubuntu/Debian/Fedora/Arch)

[![GitHub Repo](https://img.shields.io/badge/GitHub-CyberForgeEx/PowerBash-181717?logo=github)](https://github.com/CyberForgeEx/PowerBash)
[![Stars](https://img.shields.io/github/stars/CyberForgeEx/PowerBash?style=social)](https://github.com/CyberForgeEx/PowerBash)
[![PowerShell](https://img.shields.io/badge/PowerShell-5.1%2B-0072C6?logo=powershell)](https://microsoft.com/powershell)
[![Bash](https://img.shields.io/badge/Bash-4.0%2B-89e051?logo=gnu-bash)](https://gnu.org/software/bash)

---

## Project Goal

Deliver a **single, reliable, menu-driven script** that gives you the same powerful system administration capabilities whether you're on Windows PowerShell or Linux Bash perfect for:

- IT professionals • DevOps engineers  • Homelab enthusiasts  • Students

All operations are logged, color-coded, and built with rock-solid error handling.

---

#### 1. Core Utilities
Same menu — same behavior — both platforms

- `Kill Process`            → Terminate by name (smart & safe)
- `System Health Check`     → Real-time CPU + RAM usage
- `Free Space Monitoring`   → Disk usage with <30GB warning
- `File Hash (SHA256)`      → Verify integrity instantly
- `IP Geolocation Lookup`   → City, ISP, coordinates via ip-api.com
- `Network Statistics`      → Active interfaces + traffic stats
- `Timestamped Backup`      → Auto-ZIP with smart paths

#### 2. Windows-Only Bonus
- `PDF Password Protection` → AES-256 encryption via qpdf (optional)

---

## Quick Start

### Windows (PowerShell)
```powershell
# Clone and enter directory
git clone https://github.com/CyberForgeEx/PowerBash.git
cd PowerBash

# Allow script execution (once)
Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned -Force

# Run as Administrator
.\script.ps1
```

### Linux (Bash)
```bash
git clone https://github.com/CyberForgeEx/PowerBash.git
cd PowerBash

chmod +x script.sh

# Run with sudo
sudo ./script.sh
```

You’ll see the same clean interactive menu on **both** systems!

---

### Prerequisites

| Platform | Requirements |
|--------|--------------|
| **Windows** | PowerShell 5.1+, Admin rights, (Optional: qpdf via Chocolatey) |
| **Linux**   | Bash 4+, sudo, curl, zip, coreutils (pre-installed on 99% of distros) |

Install missing tools (Linux):
```bash
sudo apt update && sudo apt install curl zip coreutils
```

Install qpdf on Windows (for PDF encryption):
```powershell
choco install qpdf
```

---

## Interactive Menu (Identical on Both OS)

```
=== PowerBash - Cross-Platform System Toolkit ===
1. Kill Process
2. System Health Check
3. Free Space Monitoring
4. Retrieve File Hash (SHA256)
5. IP Location Lookup
6. Get Network Stats
7. Backup Files/Folders
8. Protect PDF with Password    (Windows only)
9. Exit
=======
Enter your choice (1-9):
```

---

## Full Logging & Auditing

Every action is automatically logged with timestamps:

**Log Location:** `./Logs/POWERBASH_YYYYMMDD.log`

**Example Log Entry:**
```
[2025-11-28 10:30:15] [SUCCESS] Terminated process: chrome (PID: 8420)
[2025-11-28 10:31:02] [WARNING] Disk / is low on space! Only 18GB free
[2025-11-28 10:32:10] [SUCCESS] Backup created: /mnt/backup/backup_20251128_103210.zip
```


---

## Feature Comparison

| Feature                  | Windows | Linux | Notes                             |
|--------------------------|---------|-------|-----------------------------------|
| Kill Process             | Yes     | Yes   | Safe, skips critical processes    |
| System Health            | Yes     | Yes   | CPU % + Memory used/total         |
| Disk Space Check         | Yes     | Yes   | Warns under 30GB                  |
| SHA256 Hash              | Yes     | Yes   | Fast, even on large files         |
| IP Geolocation           | Yes     | Yes   | Uses free ip-api.com (HTTPS)      |
| Network Stats            | Yes     | Yes   | Adapter/interface traffic         |
| Backup to ZIP            | Yes     | Yes   | Auto-timestamp + path           |
| PDF AES-256 Encryption   | Yes (qpdf) | No | Windows exclusive               |

---

## Useful While Learning / Operating

| Tool                | Purpose                                      |
|---------------------|----------------------------------------------|
| VS Code             | Edit & debug scripts                         |
| qpdf                | PDF encryption (Windows)                     |
| Task Manager / htop | Verify process kills & resource usage        |
| cron / Task Scheduler | Automate daily backups                     |

---

**Enjoy system administration that just works — everywhere.**

If PowerBash saves you time on Windows, Linux, or both please drop a star on GitHub.

[github.com/CyberForgeEx/PowerBash](https://github.com/CyberForgeEx/PowerBash)
