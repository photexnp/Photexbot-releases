# Installing Photexbot

Download the installer for your computer from the [Releases page](https://github.com/photexnp/Photexbot-releases/releases).

| System | File | How to install |
|---|---|---|
| macOS, Apple Silicon (M1–M5) | `Photexbot-<version>-macos-arm64.dmg` | Open the .dmg, drag **Photexbot** into **Applications** |
| macOS, Intel | `Photexbot-<version>-macos-x64.dmg` | Same as above |
| Windows 10/11 | `Photexbot-<version>-windows-x64.msi` | Double-click and follow the steps (no admin rights needed) |
| Windows, no install | `Photexbot-<version>-windows-x64-portable.zip` | Unzip anywhere and run `Photexbot\Photexbot.exe` |
| Ubuntu 22.04+ / Debian | `photexbot_<version>_amd64.deb` | `sudo apt install ./photexbot_<version>_amd64.deb` |

Java is bundled — nothing else to install.

## First launch

The installers are not code-signed yet, so the system will warn the first time:

- **macOS:** "Photexbot can't be opened because Apple cannot check it…". Right-click the app → **Open** → **Open**.
  (Or: System Settings → Privacy & Security → **Open Anyway**.)
- **Windows:** "Windows protected your PC". Click **More info** → **Run anyway**.

## Permissions

- **macOS — Accessibility** (needed to type into other apps): System Settings → Privacy & Security → Accessibility →
  turn on **Photexbot**. Restart Photexbot afterwards.
- **macOS — Microphone & Speech Recognition** (voice input): macOS asks the first time you press ⌘⇧Space; click Allow.
- **Ubuntu:** typing into other apps works in an **Xorg** session. On the default Wayland session, Wayland blocks
  apps from sending keystrokes to other windows. Choose "Ubuntu on Xorg" on the login screen to use form filling.

## What works where

| Feature | macOS | Windows | Ubuntu |
|---|---|---|---|
| Chat, AI providers, files (read & create) | ✅ | ✅ | ✅ |
| Form filling / typing into other apps | ✅ | ✅ | ✅ on Xorg |
| Voice input & spoken replies | ✅ | — | — |
| API keys stored in system keychain | ✅ Keychain | file in `%USERPROFILE%\.photexbot` | file in `~/.photexbot` |

Settings live in `~/.photexbot/`; files the bot creates go to `~/Documents/Photexbot/`.

## Uninstall

- **macOS:** drag Photexbot from Applications to the Trash.
- **Windows:** Settings → Apps → Photexbot → Uninstall.
- **Ubuntu:** `sudo apt remove photexbot`
