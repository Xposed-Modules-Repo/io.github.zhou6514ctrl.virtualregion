# VirtualRegion

[中文](#中文) · [English](#english)

## 中文

### 模块介绍

VirtualRegion 是一个面向用户自有设备及明确授权测试应用的 Android 8–16
LSPosed 环境虚拟化模块。模块通过统一的环境配置和按应用隔离策略，为兼容性测试、隐私测试、
自动化测试以及多地区业务验证提供可控、可恢复的测试环境。

模块采用 Modern Xposed API 102，最低支持 Android 8（API 26），目标支持 Android 16
（API 36）。界面目前以中文为主。

模块包名：`io.github.zhou6514ctrl.virtualregion`

### Telegram 群聊

加入 Telegram 群聊，获取模块更新、使用交流与问题反馈：
[https://t.me/VirtualRegion](https://t.me/VirtualRegion)

![您的支持可以让模块变得更好哦！](a.png)

### 已实现功能

- 创建、编辑、切换和保存虚拟环境配置，并保留环境历史记录。
- 按 Android 用户、应用 UID 和包名匹配策略，使不同测试应用可以使用不同环境。
- 位置环境配置，包括经纬度、精度、海拔、速度、方向和时间等常用字段。
- 地图选点、地址搜索、WGS-84 坐标跳转以及返回设备真实位置；可配置 Google 地图或高德地图。
- Wi-Fi 环境配置，包括连接信息和扫描结果所需的主要网络字段。
- 蜂窝网络与基站环境配置，覆盖常用移动网络、运营商和小区信息字段。
- SIM 环境配置，包括多卡槽、订阅和常用运营商标识字段。
- 蓝牙环境配置，包括经典蓝牙、BLE 扫描和 GATT 相关测试数据。
- LSPosed 远程配置同步、进程内原子快照缓存，以及配置变化后的实时刷新机制。
- 应用作用域管理、按应用启用或停用策略，以及可选的定位 SDK 兼容兜底。
- 系统服务状态和脱敏日志查看/导出界面。
- 针对 Android 8–16 差异的集中版本适配结构与安全失败策略。

### 当前限制

- 部分系统级 Hook 在不同厂商 ROM 上可能存在兼容性差异。
- Android 8–16 全版本、无需重启热切换、多应用隔离及长期系统稳定性仍需要更多真实设备验证。
- APK 能成功安装或构建不代表所有能力都已在每一台设备上验证。
- 建议先在备用设备或可恢复的测试环境中验证，并保留原始配置和数据备份。

### 合法与安全使用提示

本模块仅限以下场景使用：

- 您本人拥有并控制的设备；
- 设备所有者或应用所有者已明确授权的安全、兼容性、隐私或自动化测试；
- 符合所在地法律法规、服务协议和组织内部政策的研究与开发活动。

禁止将本模块用于未经授权的跟踪、身份冒用、欺诈、骚扰、规避访问控制或违反第三方权益的行为。
本项目不提供也不支持 Play Integrity 或硬件证明绕过、KYC/身份认证规避、金融/支付/政府/
紧急服务针对性规避、反作弊或风控规避，也不修改设备 HAL、驱动或固件。

位置、SIM、Wi-Fi、基站和蓝牙数据可能属于敏感信息。请仅采集必要数据，取得所需同意，限制访问，
妥善保管导出的日志与配置，并在测试结束后及时删除。使用者应自行确认其使用方式合法、获授权且不会
损害他人；因滥用造成的后果由使用者承担。

### 基本使用

1. 安装 APK，并在 LSPosed Manager 中启用模块。
2. 按实际 ROM 和测试目标选择推荐的系统服务作用域；仅在需要应用侧 SDK 兼容兜底时勾选目标应用。
3. 在模块内创建环境，并在应用管理中明确为测试应用启用对应策略。
4. 重启相关应用或进程；首次使用及版本升级后建议按设备情况重启系统。
5. 通过状态页和脱敏日志确认生效范围，测试完成后停用策略或停用模块。

---

## English

### About

VirtualRegion is an LSPosed environment-virtualization module for Android 8–16. It is
intended for user-owned devices and explicitly authorized test applications. Unified environment
profiles and per-application isolation policies provide controlled and reversible conditions for
compatibility, privacy, automation, and multi-region testing.

The module uses Modern Xposed API 102, supports Android 8 (API 26) as its minimum version, and
targets Android 16 (API 36). The application UI is currently primarily in Chinese.

Module package: `io.github.zhou6514ctrl.virtualregion`

### Telegram community

Join the Telegram community for module updates, usage discussions, and issue feedback:
[https://t.me/VirtualRegion](https://t.me/VirtualRegion)

### Implemented features

- Create, edit, switch, and store virtual environment profiles with environment history.
- Match policies by Android user, application UID, and package name so test applications can use
  separate environments.
- Configure location data, including coordinates, accuracy, altitude, speed, bearing, and time.
- Pick locations on a map, search addresses, jump to WGS-84 coordinates, and return to the real
  device location; Google Maps and AMap can be configured.
- Configure Wi-Fi connection and scan-result fields used by test environments.
- Configure common cellular network, carrier, and cell/base-station fields.
- Configure multi-SIM slots, subscriptions, and common carrier identity fields.
- Configure classic Bluetooth, BLE scan, and GATT-related test data.
- Synchronize configuration through LSPosed remote storage, maintain atomic in-process snapshots,
  and refresh policies when configuration changes.
- Manage application scope, enable or disable per-app policies, and optionally enable a
  location-SDK compatibility fallback.
- Inspect system-service status and view or export redacted logs.
- Use centralized Android 8–16 version adapters and fail-safe behavior for unsupported paths.

### Current limitations

- System-level hooks can behave differently across vendor ROMs.
- Full Android 8–16 coverage, restart-free switching, multi-app isolation, and long-term system
  stability still require broader verification on physical devices.
- A successful build or installation does not mean every feature has been verified on every device.
- Test on a spare or recoverable device first, and keep backups of original data and settings.

### Legal and safe-use notice

Use this module only on:

- devices you own and control;
- devices or applications whose owner has explicitly authorized security, compatibility, privacy,
  or automation testing; and
- research and development activities that comply with applicable law, service terms, and
  organizational policy.

Do not use this module for unauthorized tracking, impersonation, fraud, harassment, access-control
evasion, or infringement of third-party rights. This project does not provide or support Play
Integrity or hardware-attestation bypasses, KYC or identity-verification bypasses, targeted evasion
for financial, payment, government, emergency-service, anti-cheat, or risk-control systems, and it
does not modify device HALs, drivers, or firmware.

Location, SIM, Wi-Fi, cellular, and Bluetooth data may be sensitive. Collect only what is necessary,
obtain required consent, restrict access, protect exported logs and profiles, and delete test data
when it is no longer needed. Users are responsible for ensuring that their use is lawful,
authorized, and non-harmful, and remain responsible for consequences caused by misuse.

### Basic usage

1. Install the APK and enable the module in LSPosed Manager.
2. Select the required system-service scopes for the device ROM and test target. Select a target
   app only when its SDK compatibility fallback is needed.
3. Create an environment profile and explicitly enable its policy for each authorized test app.
4. Restart the affected app or process. A system reboot is recommended after first installation or
   an upgrade when required by the device.
5. Confirm the active scope through the status page and redacted logs. Disable the policy or module
   after testing.
