<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="docs/assets/lebrew-wordmark-white.png">
    <img src="docs/assets/lebrew-wordmark-black.png" alt="LEBREW" width="320">
  </picture>
</p>

<h1 align="center">LEBREW 固件升级工具</h1>

<p align="center">
  插上 USB，选好设备型号。找固件、对串口、校验下载，交给升级工具。
</p>

<p align="center">
  <a href="README.md">English</a> · <strong>简体中文</strong>
</p>

<p align="center">
  <a href="https://github.com/lebrew-tech/LEBREW-Firmware-Updater/releases/download/v1.2.0/LEBREW-Firmware-Updater.exe?download=1">
    <img src="docs/assets/download-windows.svg" alt="下载 Windows 版" width="280">
  </a>
  <a href="https://lebrew-firmware-2026.oss-ap-southeast-1.aliyuncs.com/lebrew/clients/LEBREW-Firmware-Updater-v1.2.0-macos.zip">
    <img src="docs/assets/download-macos.svg" alt="下载 macOS 版" width="280">
  </a><br>
  v1.2.0 · Windows 10/11 x64 与 macOS（Intel + Apple Silicon）。
</p>

<p align="center">
  <sub><b>macOS：</b>解压后双击 <code>LEBREW Firmware Updater.app</code>；首次打开如需系统批准，可查看 <a href="https://support.apple.com/en-us/102445">Apple 的操作说明</a>。</sub>
</p>

## 🎬 先看一段 20 秒演示

![LEBREW 固件升级工具演示](docs/demo/LEBREW-Firmware-Updater-v1.2.0-Field-Manual.gif)

<p align="center">
  v1.2.0 演示 · 20 秒 · <a href="docs/demo/LEBREW-Firmware-Updater-v1.2.0-Field-Manual-60fps.mp4">查看 60 fps 高清版</a> · <a href="docs/demo/LEBREW-Firmware-Updater-Field-Manual-60fps.mp4">旧版演示</a>
</p>

## ✨ v1.2.0 有哪些新鲜事？

- ⬆️ **升级工具也能给自己升级。** 点击顶栏「检查 App 更新」。Windows 和 macOS 发布版检测到新版本后，可在 App 内下载、校验和安装。从旧版升级时，请先手动安装一次 v1.2.0。
- 🧰 **日常升级和售后恢复，各有入口。** 「下载并烧录」默认只更新设备主程序。售后恢复时，可开启右下角的「完整烧录」。工具会核对设备分区布局，保留标定和设备设置。
- 🔄 **想重启设备，按一下就好。** 「单独复位」会重启当前串口连接的设备。
- 👀 **产品列表来了两张新面孔。** 产品列表第一是 **BrewMaster Linea** 智能咖啡电子秤，第二是 **AquaDou** 咖啡二合一检测仪，均标注「即将发售」。
- ✨ **打开 App，先看大字标。** 内置 LEBREW 大字标从两侧汇聚，按钮按下时有动画反馈。

[v1.2.0 发布说明和校验值](https://github.com/lebrew-tech/LEBREW-Firmware-Updater/releases/tag/v1.2.0)

## 🧭 固件更新不该像开盲盒

固件在一个文件夹，烧录工具在另一个。USB 一插，串口列表又多了几项。型号、版本或串口选错，都可能让设备无法启动。

用升级工具时，跟着这一条路线走就行。

> **选择产品 → 使用最新版本 → 识别设备 → 校验下载 → 开始烧录 → 重启确认**

## 🔧 哪些活儿可以交给它

- **产品引导选择**：用产品缩略图和名称帮助客户选中正确型号。
- **默认最新版本**：默认使用最新固件，需要回退时仍可选择历史版本。
- **设备自动匹配**：识别兼容的 USB 设备，并对应到产品与串口。
- **多设备清楚区分**：连接多台设备时分别列出，点击即可切换。
- **下载完整性校验**：烧录前检查固件包；校验失败立即停止更新。
- **安全更新模式**：日常更新保留设备现有设置，完整恢复则作为单独选项。
- **中英文界面**：无需退出软件即可切换语言。
- **本地固件兜底**：在线更新不可用时，可以选择本地固件包。

## 🚀 从插线到重启，五步走

1. 通过 USB 连接设备。
2. 选择产品型号。
3. 确认最新版本和识别到的串口。
4. 下载、校验并烧录。
5. 等待设备自动重启。

界面会同时显示产品、版本、校验结果、串口、更新模式和当前状态，让每一步都有明确依据。

## 🛡️ 点下烧录键，工具先把关

- 开始烧录前先验证下载内容。
- 默认更新主程序。开启完整烧录后，工具会先核对设备分区布局。
- 烧录前把产品、版本和串口放在一起确认。
- 客户不需要理解芯片地址或命令行参数。

## 💻 选你的电脑版本

| 平台 | 状态 |
| --- | --- |
| Windows | 已提供 — 已打包桌面程序 |
| macOS | 已提供 — Intel 与 Apple Silicon 通用版 |

最新版 GitHub Release 提供 Windows 安装包和 macOS 下载链接。macOS 通用版采用临时签名，未做 Apple 公证。首次打开可参考 [Apple 的操作说明](https://support.apple.com/en-us/102445)。

当前 Windows 版本未做数字签名，Windows SmartScreen 可能显示提示。

## 🛟 卡住了？看这里

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

☕ 可以喝口咖啡，等设备重启完成再拔 USB。
