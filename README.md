# VirtualRegion

[中文](#中文) | [English](#english)

> [!WARNING]
> **使用地区限制 / Regional Usage Restriction**
>
> **中文：本模块不允许在中国使用，因此采用 Telegram 群组授权验证。**
>
> **English: This module is not permitted for use in China. Authorization is therefore verified through the Telegram group.**

## 中文

VirtualRegion 可以为手机里的不同应用设置独立的虚拟环境，适合在自己的设备上进行应用测试。

当前版本：[0.2.4](https://github.com/Xposed-Modules-Repo/io.github.zhou6514ctrl.virtualregion/releases/tag/15-0.2.4)

## 主要功能

- 在地图上选择位置，也可以搜索地点或直接输入坐标。
- 为不同应用设置不同的位置，互不影响。
- 设置应用看到的 Wi-Fi 信息和附近 Wi-Fi 列表。
- 设置应用看到的手机卡、运营商、信号和基站信息。
- 设置应用看到的经典蓝牙和低功耗蓝牙设备。
- 创建多个环境，一键切换需要使用的环境。
- 导出全部环境作为备份，也可以重新导入。
- 从当前手机读取环境信息，减少手动填写。
- 单独控制每个应用需要启用的功能。
- 查看当前状态和运行记录，方便判断是否已经生效。
- 支持中文和英文界面。
- 蓝牙环境记录更完整，虚拟蓝牙设备列表显示更齐全。
- 虚拟蓝牙会持续返回设备，扫描停止后不会继续返回旧结果。
- 支持为不同应用分别选择固定位置或路线模拟，并独立控制路线进度与速度。
- 路线可通过地图绘制、地图规划或真实移动录制创建。
- 路线录制使用当前地图服务商的联合定位，支持长时间增量保存和中断恢复。
- 路线播放会同步模拟 GPS、Wi-Fi、基站与标准 GNSS 卫星状态。
- 改善路线编辑、录制状态、弹窗界面和 Android 16 定位兼容性。

## 简单使用

1. 下载并安装最新 APK。
2. 在 LSPosed 中启用 VirtualRegion，然后重启手机。
3. 打开 VirtualRegion，按提示完成授权。
4. 创建一个环境并填写需要的信息。
5. 在应用管理中选择目标应用和对应环境。
6. 保存后重新打开目标应用。

第一次安装或升级后，建议重启一次手机。不同品牌和系统版本的表现可能不同，请先在备用设备上测试。

## 获取更新和帮助

Telegram：[https://t.me/VirtualRegion](https://t.me/VirtualRegion)

## 使用提醒

请只在自己拥有的设备或已经得到明确许可的测试设备上使用。不要用于欺骗、盗取信息、干扰他人或其他违法用途。

---

## English

VirtualRegion lets you set a separate virtual environment for different apps on your phone. It is intended for app testing on devices you own or are authorized to use.

Current version: [0.2.4](https://github.com/Xposed-Modules-Repo/io.github.zhou6514ctrl.virtualregion/releases/tag/15-0.2.4)

## Main Features

- Choose a location on the map, search for a place, or enter coordinates.
- Give different apps different locations without affecting each other.
- Set the Wi-Fi connection and nearby Wi-Fi networks visible to an app.
- Set SIM card, carrier, signal, and cell tower information visible to an app.
- Set classic Bluetooth and Bluetooth Low Energy devices visible to an app.
- Create multiple environments and switch between them easily.
- Export all environments as a backup and import them again later.
- Read environment information from the current phone to reduce manual input.
- Choose which features are enabled for each app.
- View status and activity records to check whether your settings are active.
- Use the app in Chinese or English.
- Keep more complete Bluetooth environment data and show the full virtual device list.
- Keep returning Bluetooth devices during a scan and stop old results after scanning ends.
- Choose fixed-location or route simulation independently for each app, with separate route progress and speed controls.
- Create routes by drawing on the map, using map route planning, or recording real movement.
- Record routes with the selected map provider's fused location source, long-session journaling, and interrupted-session recovery.
- Keep GPS, Wi-Fi, cell, and standard GNSS satellite status consistent during route playback.
- Improved route editing, recording status, dialog styling, and Android 16 location compatibility.

## Quick Start

1. Download and install the latest APK.
2. Enable VirtualRegion in LSPosed, then restart your phone.
3. Open VirtualRegion and follow the authorization prompt.
4. Create an environment and enter the information you need.
5. Select the target app and environment in app management.
6. Save the settings and reopen the target app.

Restarting the phone once is recommended after the first installation or an update. Results may vary between phone brands and system versions, so test on a spare device first.

## Updates and Help

Telegram: [https://t.me/VirtualRegion](https://t.me/VirtualRegion)

## Usage Notice

Use VirtualRegion only on devices you own or test devices for which you have clear permission. Do not use it for deception, data theft, disruption, or any illegal activity.
