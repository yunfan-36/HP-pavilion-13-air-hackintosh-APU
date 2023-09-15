# hp-pavilion-13-air-hackintosh




尚未实现功能：

1.硬件解码

2.休眠
[![](https://img.shields.io/badge/macOS-Ventura_13.4.1-orange.svg)](https://www.apple.com/macos/ventura/)
[![](https://img.shields.io/badge/OpenCore-0.9.3-blue.svg)](https://github.com/acidanthera/OpenCorePkg)
[![](https://img.shields.io/badge/translation-english-green.svg)](./docs/README_EN.md)

<img src="./docs/about-this-mac.jpg" style="height: 50vh" />

## ⚙️ 硬件规格
##### 电脑产品系列：HP Pavilion Aero Laptop 

##### 电脑产品型号：13-be1xxx

##### 主板ID：89FA
##### 使用Smokeless-UMAF修改过bios，开启游戏模式，将显卡显存由512M调整为2G，如果不修改使用视频软件如vlc、iina会蓝屏卡顿，软件报错退出。

| 类别 | 型号                                                         |
| ---- | ------------------------------------------------------------ |
| CPU  | AMD 5625U                                                    |
| GPU  | AMD Radeon 7 Graphics (Renoir)                               |
| 网卡 | intel AX210 |

## 🚀 功能情况

| Category    | Status                 |
| ----------- | ---------------------- |
| 核显        | ✅ **但不支持硬件加速** |
| WiFi        | ✅                      |
| 蓝牙        | ✅                      |
| 扬声器      | ✅                      |
| 麦克风      | ❌                      |
| 摄像头      | ✅                      |
| Fn 功能     | ✅ 亮度、音量调节支持   |
| USB、Type-C | ✅ 支持供电、外接显示器 |
| 睡眠        | ✅ S25                   |


## 🔧 需要自己生成的

### UTBMap

- 定制 USB 端口
- [官方仓库](https://github.com/USBToolBox/tool/)
- 操作指引：[文档](https://apple.sqlsec.com/6-%E5%AE%9E%E7%94%A8%E5%A7%BF%E5%8A%BF/6-1/)

### SSDTTime

- 生成 ACPI
- [官方仓库](https://github.com/corpnewt/SSDTTime)
- 操作指引：[视频](https://www.bilibili.com/video/BV1iN41167Jk)

### SSDT-SBUS-MCHC

- 可能不是必须，如果第一次 boot installer 时出错可以尝试这块内容

- 操作指引：[文档](https://dortania.github.io/Getting-Started-With-ACPI/Universal/smbus.html)

## 🛸 注意事项

### AMD_Vanilla Patch

- [官方仓库](https://github.com/AMD-OSX/AMD_Vanilla)
- 5600U 为 6 核心 CPU，如果为其他 CPU 参考本 EFI，需要根据官方仓库的 README，或是[参考视频](https://www.bilibili.com/video/BV1Vh4y1375g)中的说明，根据核心数修改 Patch 的数值

### 硬件加速

- 截止目前所使用的 [NootedRed](https://github.com/NootInc/NootedRed/actions/runs/5425999871) 版本（CI\#957）还未支持硬件加速
- Chrome、VS Code 都需要关闭硬件加速的设置（[参考](https://nootinc.github.io/nred#chrome-chromium-based-browsers-and-apps-like-sublime-text-cause-graphical-artefacts-amongst-other-problems)）
- 视频播放可以使用 Safari
