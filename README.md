<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="docs/assets/lebrew-wordmark-white.png">
    <img src="docs/assets/lebrew-wordmark-black.png" alt="LEBREW" width="320">
  </picture>
</p>

<h1 align="center">LEBREW Firmware Updater</h1>

<p align="center">
  A clearer, safer way to keep LEBREW devices up to date.
</p>

<p align="center">
  <strong>English</strong> · <a href="README.zh-CN.md">简体中文</a>
</p>

<p align="center">
  <a href="https://github.com/lebrew-tech/LEBREW-Firmware-Updater/releases/latest/download/LEBREW-Firmware-Updater.exe">
    <img src="docs/assets/download-windows.svg" alt="Download for Windows" width="280">
  </a>
  <a href="https://github.com/lebrew-tech/LEBREW-Firmware-Updater/releases/latest/download/LEBREW-Firmware-Updater-macos-universal.zip">
    <img src="docs/assets/download-macos.svg" alt="Download for macOS" width="280">
  </a><br>
  Windows 10/11 and macOS (Intel + Apple Silicon) · direct download from the latest release.
</p>

<p align="center">
  <sub><b>macOS:</b> unzip → double-click <code>LEBREW Firmware Updater.app</code>. If macOS blocks it, right-click → <b>Open</b>.</sub>
</p>

![LEBREW Firmware Updater product walkthrough](docs/demo/LEBREW-Firmware-Updater-Field-Manual.gif)

<p align="center">
  20-second walkthrough · <a href="docs/demo/LEBREW-Firmware-Updater-Field-Manual-60fps.mp4">Watch the 60 fps version</a>
</p>

## Firmware updates should not feel like a guessing game

Finding the right firmware, choosing the right port and entering the right flash options used to require several tools and a lot of manual checking. One wrong choice can leave a device unable to boot.

LEBREW Firmware Updater turns that process into one guided flow for customers, sales and support teams:

> **Choose a product → use the latest version → detect the device → verify the download → flash → restart**

## What it handles

- **Guided product selection** — recognizable product cards make the correct model easy to choose.
- **Latest version by default** — older builds stay available when a rollback is needed.
- **Device-aware matching** — compatible USB devices are identified and matched to their product and port.
- **Clear multi-device handling** — when several devices are connected, each one is listed separately for selection.
- **Verified downloads** — every package is checked before flashing; a failed check stops the update.
- **Safe update modes** — routine updates preserve existing device settings; full recovery is a separate, explicit choice.
- **English and Chinese UI** — switch language without leaving the app.
- **Local fallback** — a local firmware package can be selected when an online update is unavailable.

## Five steps

1. Connect the device over USB.
2. Choose the product model.
3. Confirm the latest version and detected port.
4. Download, verify and flash.
5. Wait for the automatic restart.

The interface keeps the important states visible: selected model, firmware version, checksum result, serial port, update mode and current status.

## Built for fewer avoidable mistakes

- Downloads are validated before any flashing begins.
- The routine update path is the default; destructive recovery is never accidental.
- Product, version and port are shown together before the update starts.
- The app is designed to work without asking customers to learn chip addresses or command-line tools.

## Platform

| Platform | Status |
| --- | --- |
| Windows | Available — packaged desktop application |
| macOS | Available — universal build for Intel and Apple Silicon (unsigned) |

Both builds are available from the latest GitHub Release. The macOS build is universal (Intel + Apple Silicon) but unsigned and not notarized, so the first launch needs a right-click → Open.

The current Windows build is unsigned, so Windows SmartScreen may show a warning.

## Troubleshooting

- **Error 2:** if the log says `FileNotFoundError(2)`, reconnect USB, detect the device again and select the current port. Close other serial apps.
- **Download or checksum failed:** check your connection and download again. Do not skip verification.
- **Still stuck:** copy the run log and include your updater version, product model and exact error when contacting support.

[Detailed errors and fixes (English)](https://github.com/lebrew-tech/LEBREW-Firmware-Updater/issues/2) · [中文](https://github.com/lebrew-tech/LEBREW-Firmware-Updater/issues/1)

## About this repository

This is a **public product showcase**, not the product source repository. It intentionally does not contain proprietary source code, firmware images, release tooling, credentials or internal infrastructure details.

The walkthrough uses sample product and version data. Product names, logos and imagery belong to LEBREW.

## Learn more

[lebrewtech.com](https://lebrewtech.com/)

---

**Choose the model. Let the updater do the rest.**
