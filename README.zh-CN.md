<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="docs/assets/lebrew-wordmark-white.png">
    <img src="docs/assets/lebrew-wordmark-black.png" alt="LEBREW" width="320">
  </picture>
</p>

<h1 align="center">LEBREW 固件升级工具</h1>

<p align="center">
  让 LEBREW 设备的固件更新更清楚、更安全。
</p>

<p align="center">
  <a href="README.md">English</a> · <strong>简体中文</strong>
</p>

<p align="center">
  <a href="https://github.com/lebrew-tech/LEBREW-Firmware-Updater/releases/latest/download/LEBREW-Firmware-Updater.exe">
    <img src="docs/assets/download-windows.svg" alt="下载 Windows 版" width="280">
  </a>
  <a href="https://github.com/lebrew-tech/LEBREW-Firmware-Updater/releases/latest/download/LEBREW-Firmware-Updater-macos-universal.zip">
    <img src="docs/assets/download-macos.svg" alt="下载 macOS 版" width="280">
  </a><br>
  Windows 10/11 与 macOS（Intel + Apple Silicon）· 点击即从最新 Release 直接下载。
</p>

<p align="center">
  <sub><b>macOS：</b>解压后双击 <code>LEBREW Firmware Updater.app</code>；首次被拦截就右键 →「打开」。</sub>
</p>

![LEBREW 固件升级工具演示](docs/demo/LEBREW-Firmware-Updater-Field-Manual.gif)

<p align="center">
  20 秒功能演示 · <a href="docs/demo/LEBREW-Firmware-Updater-Field-Manual-60fps.mp4">查看 60 fps 高清版</a>
</p>

## 固件更新不该像开盲盒

过去更新固件，往往要在多个工具之间切换：先确认产品型号，再找对应版本，检查芯片、串口和烧录方式。任何一步选错，都可能让设备无法启动。

LEBREW 固件升级工具把这条容易出错的流程整理成一次清楚的引导：

> **选择产品 → 使用最新版本 → 识别设备 → 校验下载 → 开始烧录 → 重启确认**

## 它负责什么

- **产品引导选择**：用产品缩略图和名称帮助客户选中正确型号。
- **默认最新版本**：默认使用最新固件，需要回退时仍可选择历史版本。
- **设备自动匹配**：识别兼容的 USB 设备，并对应到产品与串口。
- **多设备清楚区分**：连接多台设备时分别列出，点击即可切换。
- **下载完整性校验**：烧录前检查固件包；校验失败立即停止更新。
- **安全更新模式**：日常更新保留设备现有设置，完整恢复则作为单独选项。
- **中英文界面**：无需退出软件即可切换语言。
- **本地固件兜底**：在线更新不可用时，可以选择本地固件包。

## 五步完成更新

1. 通过 USB 连接设备。
2. 选择产品型号。
3. 确认最新版本和识别到的串口。
4. 下载、校验并烧录。
5. 等待设备自动重启。

界面会同时显示产品、版本、校验结果、串口、更新模式和当前状态，让每一步都有明确依据。

## 减少本可避免的失误

- 开始烧录前先验证下载内容。
- 默认走常规更新路径，不会轻易触发破坏性恢复。
- 烧录前把产品、版本和串口放在一起确认。
- 客户不需要理解芯片地址或命令行参数。

## 支持平台

| 平台 | 状态 |
| --- | --- |
| Windows | 已提供 — 已打包桌面程序 |
| macOS | 已提供 — Intel 与 Apple Silicon 通用版（未签名） |

Windows 与 macOS 版本均可从最新 GitHub Release 下载。macOS 为通用版（Intel + Apple Silicon），但未签名、未公证，首次打开需右键「打开」。

当前 Windows 版本未做数字签名，Windows SmartScreen 可能显示提示。

## 常见问题

- **错误码 2**：日志含 `FileNotFoundError(2)` 时，重新插拔 USB、重新识别并选择当前串口，同时关闭其他串口软件。
- **下载或校验失败**：检查网络后重新下载，不要跳过校验。
- **仍然失败**：复制运行记录，联系支持时提供工具版本、产品型号和完整报错。

[详细报错与解决办法（中文）](https://github.com/lebrew-tech/LEBREW-Firmware-Updater/issues/1) · [English](https://github.com/lebrew-tech/LEBREW-Firmware-Updater/issues/2)

## 关于这个仓库

这是一个**公开产品展示仓库**，不是产品源码仓库。这里不会包含专有源代码、固件文件、发布工具、凭据或内部基础设施信息。

演示中使用的是示例产品和版本数据。产品名称、Logo 与图片归 LEBREW 所有。

## 了解更多

[lebrewtech.com](https://lebrewtech.com/)

---

**选对型号，剩下的交给工具。**
