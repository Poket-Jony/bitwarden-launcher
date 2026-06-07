# Bitwarden Launcher

[![Bitwarden](https://img.shields.io/badge/Bitwarden-2026.5.0-blue.svg)](https://github.com/bitwarden/clients/releases/tag/desktop-v2026.5.0)

Bitwarden Launcher (Autostart Minimized) for macOS.

>Starting with [Bitwarden 2026.5.0](https://github.com/bitwarden/clients/releases/tag/desktop-v2026.5.0), the minimized autostart feature has been removed from the client UI. This feature is now supposed to work automatically, but it does not on macOS. This launcher opens Bitwarden with the required `--autostart` option, ensuring that Bitwarden starts minimized again.

## Setup
1. Download and Mount [Bitwarden Launcher.dmg](Bitwarden Launcher.dmg)
2. Copy `Bitwarden Launcher.app` to `/Applications/Bitwarden Launcher.app`
3. Open System Settings and navigate to `General` → `Login Items & Extensions`
4. Click the + (Plus) button and select `Bitwarden Launcher.app`

## Content
The app is a simple Automator script:

```shell
open -a /Applications/Bitwarden.app --args --autostart
```

## Sources
- https://github.com/bitwarden/clients/issues/20923
- https://github.com/bitwarden/clients/issues/21074
