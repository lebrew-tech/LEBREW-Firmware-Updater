<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="docs/assets/lebrew-wordmark-white.png">
    <img src="docs/assets/lebrew-wordmark-black.png" alt="LEBREW" width="320">
  </picture>
</p>

<h1 align="center">LEBREW Firmware Updater</h1>

<p align="center">
  Plug in over USB and pick your LEBREW model. The updater finds the firmware and checks it before flashing.
</p>

<p align="center">
  <strong>English</strong> · <a href="README.zh-CN.md">简体中文</a>
</p>

<p align="center">
  <a href="https://github.com/lebrew-tech/LEBREW-Firmware-Updater/releases/download/v1.2.0/LEBREW-Firmware-Updater.exe?download=1">
    <img src="docs/assets/download-windows.svg" alt="Download for Windows" width="280">
  </a>
  <a href="https://lebrew-firmware-2026.oss-ap-southeast-1.aliyuncs.com/lebrew/clients/LEBREW-Firmware-Updater-v1.2.0-macos.zip">
    <img src="docs/assets/download-macos.svg" alt="Download for macOS" width="280">
  </a><br>
  v1.2.0 · Windows 10/11 x64 and macOS (Intel + Apple Silicon).
</p>

<p align="center">
  <sub><b>macOS:</b> unzip → double-click <code>LEBREW Firmware Updater.app</code>. If macOS asks for approval, see <a href="https://support.apple.com/en-us/102445">Apple’s first-launch instructions</a>.</sub>
</p>

## 🎬 A 20-second look around

![LEBREW Firmware Updater product walkthrough](docs/demo/LEBREW-Firmware-Updater-v1.2.0-Field-Manual.gif)

<p align="center">
  v1.2.0 walkthrough · 20 seconds · <a href="docs/demo/LEBREW-Firmware-Updater-v1.2.0-Field-Manual-60fps.mp4">Watch the 60 fps version</a> · <a href="docs/demo/LEBREW-Firmware-Updater-Field-Manual-60fps.mp4">Previous walkthrough</a>
</p>

## ✨ Fresh in v1.2.0

- ⬆️ **The updater can update itself.** Select **Check app updates** in the toolbar. When a newer release is available, the packaged Windows and macOS apps can download, verify and install it. Install v1.2.0 manually once if you are upgrading from an older release.
- 🧰 **One button for everyday updates, one toggle for recovery.** **Download & flash** updates the device's main program by default. Enable the small **Full flash** toggle for recovery. It checks the device's flash layout and preserves calibration and settings.
- 🔄 **Give the device a quick restart.** **Reset device** restarts the device on the selected USB port.
- 👀 **Two new faces in the product picker.** The picker puts **BrewMaster Linea** (smart coffee scale) first and **AquaDou** (two-in-one coffee analyzer) second. Both are marked **Coming Soon**.
- ✨ **A new entrance for the LEBREW wordmark.** The built-in LEBREW wordmark animates in from both sides. Buttons now animate on press.

[v1.2.0 release notes and checksums](https://github.com/lebrew-tech/LEBREW-Firmware-Updater/releases/tag/v1.2.0)

## 🧭 Firmware updates, minus the guessing game

The firmware is in one folder, the flashing tool is in another, and plugging in USB has just added a few more port names to the list. Pick the wrong combination and the device may fail to boot.

Here’s the route the updater gives customers, sales and support teams.

> **Choose a product → use the latest version → detect the device → verify the download → flash → restart**

## 🔧 What the updater handles

- **Guided product selection** — recognizable product cards make the correct model easy to choose.
- **Latest version by default** — older builds stay available when a rollback is needed.
- **Device-aware matching** — compatible USB devices are identified and matched to their product and port.
- **Clear multi-device handling** — when several devices are connected, each one is listed separately for selection.
- **Verified downloads** — every package is checked before flashing; a failed check stops the update.
- **Safe update modes** — routine updates preserve existing device settings; full recovery is a separate, explicit choice.
- **English and Chinese UI** — switch language without leaving the app.
- **Local fallback** — a local firmware package can be selected when an online update is unavailable.

## 🚀 From USB to restart in five steps

1. Connect the device over USB.
2. Choose the product model.
3. Confirm the latest version and detected port.
4. Download, verify and flash.
5. Wait for the automatic restart.

The interface keeps the important states visible: selected model, firmware version, checksum result, serial port, update mode and current status.

## 🛡️ Before you press Flash

- Downloads are validated before any flashing begins.
- The main-program update is the default. Full flash is an explicit choice and checks the device layout.
- Product, version and port are shown together before the update starts.
- The app is designed to work without asking customers to learn chip addresses or command-line tools.

## 💻 Pick your platform

| Platform | Status |
| --- | --- |
| Windows | Available — packaged desktop application |
| macOS | Available — universal build for Intel and Apple Silicon |

The latest GitHub Release links to the Windows executable and the macOS download. The macOS build uses an ad-hoc signature and is not notarized. See [Apple’s first-launch instructions](https://support.apple.com/en-us/102445).

The current Windows build is unsigned, so Windows SmartScreen may show a warning.

## 🛟 When a step gets stuck

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

☕ Take a sip while the device restarts. Unplug the USB cable once the restart is complete.
