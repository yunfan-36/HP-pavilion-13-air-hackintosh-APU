# HP-pavilion-13-air-hackintosh

## ⚙️ 硬件规格
- 电脑产品系列：HP Pavilion Aero Laptop 
- 电脑产品型号：13-be1xxx
- 主板ID：89FA

| 类别 | 型号                                                         |
| ---- | ------------------------------------------------------------ |
| CPU  | AMD 5625U                                                    |
| GPU  | AMD Radeon 7 Graphics (Renoir)                               |
| 网卡 | Intel AX210 |

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

## 🛸 注意事项

### bios设置
- 使用Smokeless-UMAF修改过bios，开启游戏模式，将显卡显存由512M调整为2G，如果不修改使用视频软件如vlc、iina会蓝屏卡顿，软件报错退出。
- 网卡更换为Intel AX210。

### 硬件加速

- 截止目前所使用的 [NootedRed]还未支持硬件加速
- Chrome、VSCode、vlc、iina 都需要关闭硬件加速的设置（[参考](https://nootinc.github.io/nred#chrome-chromium-based-browsers-and-apps-like-sublime-text-cause-graphical-artefacts-amongst-other-problems)）
