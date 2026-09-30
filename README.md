# Antminer Firmware Updater by MineMoreBtc

**Free Windows tool to batch-update Bitmain Antminer firmware across a whole fleet.**
Scan a subnet, test on a few miners, then flash the rest in parallel. Pools and worker names are kept.

**[⬇ Download the latest release](https://github.com/GoldingenTech/antminer-firmware-updater/releases/latest)** · [Product page](https://minemorebtc.com/tools/antminer-firmware-updater/) · [Telegram](https://t.me/goldingen_software)

---

## Features

- **Subnet scan**: ranges, CIDR (`/23`), or several saved ranges at once, up to 65,536 addresses
- **Auto-matching**: each miner is matched to the right official `.bmu` file by model and control board, including merged multi-board files
- **Test-first**: update a few miners per board type before the rest of the fleet
- **Parallel flashing**, with optional version verification after reboot
- **Keep miner settings** (pools, workers, network) is on by default
- **Safe stop**: a miner mid-upload always finishes its transfer
- **Restart / sleep / wake** in bulk
- **Mixed-fleet inventory**: also detects WhatsMiner, Avalon, Sealminer, Braiins OS, LuxOS, Auradine
- `inventory.csv` export, per-miner scan history, and a **command-line version**

## Quick start

1. Download `MMB-FirmwareUpdater_<version>.zip` from [Releases](https://github.com/GoldingenTech/antminer-firmware-updater/releases/latest) and unzip the **whole folder** (the exes need `_internal` next to them).
2. Put official Bitmain `.bmu` files next to the app or in a `firmware` subfolder ([Bitmain firmware downloads](https://service.bitmain.com/support/download?product=Antminer)). No firmware is bundled.
3. Run `MMB-FirmwareUpdater.exe`, scan your IP range, update test miners, then update the rest.

> **SmartScreen:** the app isn't code-signed yet. Click *More info → Run anyway*.

## Verify your download

Every release has a `.zip.sha256` file next to the zip, and the hash is also published on the [product page](https://minemorebtc.com/tools/antminer-firmware-updater/#verify). Inside the zip, `SHA256SUMS.txt` lists the hash of every file.

```powershell
Get-FileHash .\MMB-FirmwareUpdater_260930.1451.zip -Algorithm SHA256
```

## User guide

An 18-page PDF user guide (`MMB-FirmwareUpdater_User_Guide.pdf`) is included in the zip.

## Requirements

Windows 10/11 64-bit, on the same LAN or VPN as the miners. No installation and no internet connection needed. No telemetry.

## Licence & disclaimer

Freeware, closed source. Free to use, including commercially. Provided "as is", without warranty. You use it at your own risk: MineMoreBtc / Goldingen Tech are not liable for any damage, including bricked miners, lost settings or downtime. Antminer and Bitmain are trademarks of their respective owners. This project is not affiliated with Bitmain.

---

Built by the team behind **[MineMoreBtc (MMB)](https://minemorebtc.com)**, an on-premise platform for managing whole Bitcoin mining sites.
