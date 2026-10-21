# Flight Scraper for Windows

[Download the latest installer](https://github.com/santistebanc/flight-scraper-releases/releases/latest)

This repository contains Windows installers, signed update manifests, checksums and release notes. The application source is maintained in a separate private repository.

## Install

Download the setup executable from the latest release and run it. Python, Node and Rust are bundled; you do not need to install them. The installer checks for Microsoft WebView2 and can download it if it is missing.

The app targets Windows 10/11 x64 and Windows 11 ARM64 through x64 emulation.

## Updates

Version 0.3.2 and later check for updates at startup and every six hours. Updates download in the background and are verified against the app's embedded signing key. Open **App updates** in the toolbar to restart and install, check now, or change update preferences. Automatic installation at startup is optional. Active searches and verification windows must finish before installation.

If you installed an earlier version, install the latest release once to enable future updates through the app. Updates preserve saved searches and preferences.

## Signatures

The `.exe.sig` file is a Tauri update signature. It protects the update process and is separate from Windows publisher signing. Current installers are not Authenticode signed, so Windows may display an unknown publisher or SmartScreen warning.

`SHA256SUMS.txt` provides the installer checksum. `latest.json` is consumed by the app's updater.