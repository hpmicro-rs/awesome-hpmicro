# Awesome HPMicro

非官方 HPMicro MCU 相关资源精选列表。

## 官方资源

- 主页：[先楫半导体 HPMicro](https://www.hpmicro.com/)
  - 数据手册、用户手册、勘误表、设计指南、KiCAD封装：[设计资源/芯片资料](https://www.hpmicro.com/resources/resources.html)
  - 论坛：[先楫社区](https://www.hpmicro.com/support/forumpark.html)
- 在线商店：[在线购买](https://www.hpmicro.com/support/shop.html)
- **百度网盘资源**：[百度网盘](https://pan.baidu.com/s/1RaYHOD7xk7fnotmgLpoAlA?pwd=xk2n)
- [引脚复用工具 pinmux](https://tools.hpmicro.com/pinmux)
- [哔哩哔哩 - 先楫半导体HPMicro](https://space.bilibili.com/1306310554)
- 微信公众号：先楫半导体HPMicro

### 官方仓库

- GitHub 组织：[GitHub - hpmicro](https://github.com/hpmicro)
- Gitee 镜像：[HPMicro 官方镜像](https://gitee.com/hpmicro)
- **官方SDK**：[hpmicro/hpm_sdk](https://github.com/hpmicro/hpm_sdk)
  - HPM SDK文档（中文）：[HPM SDK 文档](https://hpm-sdk.readthedocs.io/zh-cn/latest/)
  - HPM SDK文档（英文）：[HPM SDK Documentation](http://doc.hpmicro.com/sdk_doc/en/latest/html/index.html)
- Arduino 支持：[hpmicro/arduino](https://github.com/hpmicro/arduino)
- HPMicro 烧写工具：[hpm_manufacturing_tool](https://github.com/hpmicro/hpm_manufacturing_tool)
- OpenOCD 分支：[hpmicro/riscv-openocd](https://github.com/hpmicro/riscv-openocd)
  - 相应的配置文件位于 `hpm_sdk/boards/openocd/`
- VSCode扩展：[hpm_pinmux_tool](https://github.com/hpmicro/hpm_pinmux_tool) - 自2023年9月27日起未更新，请使用引脚复用工具代替。

### 第三方 RTOS 支持

- Zephyr: [zephyrproject-rtos/hal_hpmicro](https://github.com/zephyrproject-rtos/hal_hpmicro)
- NuttX: [hpmicro/nuttx](https://github.com/hpmicro/nuttx)
  - [hpmicro/nuttx_apps](https://github.com/hpmicro/nuttx_apps)
- RT-Thread: [RT-Thread/rt-thread/bsp/hpmicro](https://github.com/RT-Thread/rt-thread/tree/master/bsp/hpmicro)

### IDE 支持

- [SEGGER Embedded Studio for RISC-V and ARM](https://www.segger.com/downloads/embedded-studio/#embeddedstudio)
  - HPMicro 许可证申请：<https://license.segger.com/hpmicro.cgi>

## IP 核

RISC-V IP 核心由 晶心科技(Andes Technology Corporation)提供。

- [Andes产品文档](http://www.andestech.com/en/products-solutions/product-documentation/)
  - HPMicro 使用的 IP 核是 D25(F)(用于HPM5xxx) 和 D45(用于HPM6xxx)

M_CAN IP核心由Bosch提供。

- 介绍和文档 [M_CAN - Bosch](https://www.bosch-semiconductors.com/ip-modules/can-ip-modules/m-can/)

EtherCAT 从站控制器 IP 核由 倍福(Beckhoff Automation) 提供。

- PDF [第一部分 – 技术](https://download.beckhoff.com/download/document/io/ethercat-development-products/ethercat_esc_datasheet_sec1_technology_2i3.pdf)
- PDF [第二部分 - 寄存器描述](https://download.beckhoff.com/download/document/io/ethercat-development-products/ethercat_esc_datasheet_sec2_registers_3i0.pdf)

## 芯片系列

请参考: [hpm-data]

## 开发板

| 开发板         | MCU     | FLASH | 外部 RAM   | USB          | 用户LED         | 用户按钮         | GPIO 接口            | 以太网   | 其他                                                    |
|----------------|---------|-------|------------|--------------|-----------------|------------------|----------------------|----------|---------------------------------------------------------|
| hpm5300evklite | HPM5301 | 1MB   | -          | 1 USB, 1 UART| 1 Red           | 1 Boot, 1 User   | RPi                  | -        |                                                         |
| hpm5300evk     | HPM5361 | 1MB   | -          | 1 USB, 1 DBG | 1 Red           | 1 User, 1 WBUTN  | RPi, Motor 32pin     | -        | ADC, CAN, LIN, 485, 422                                 |
| hpm6200evk     | HPM6280 | 16MB  | -          | 1 USB, 1 DBG | 1 RGB           | 1 PBUTN          | ART-Pi, Motor 20pin  | -        | ADC, HRPWM                                              |
| hpm6300evk     | HPM6360 | 16MB  | 32MB SDRAM | 1 USB, 1 DBG | 1 Green         | 1 PBUTN, 1 WBUTN | RPi, Motor 20pin     | 100M     | TF卡, CAN                                               |
| hpm6750evk     | HPM6750 | 16MB  | 32MB SDRAM | 2 USB, 1 DBG | 1 RGB           | 1 PBUTN, 1 WBUTN | 12pin, Motor 20pin   | 1G, 100M | LCD/TP, DVP, TF卡, CAN, Audio, Buzzer                   |
| hpm6750evk2    | HPM6750 | 16MB  | 32MB SDRAM | 2 USB, 1 UART| 1 RGB           | 1 PBUTN, 1 WBUTN | 12pin, Motor 20pin   | 1G, 100M | LCD/TP, DVP, TF卡, CAN, Audio                           |
| hpm6750evkmini | HPM6750 | 8MB   | 16MB SDRAM | 1 USB, 1 DBG | 1 RGB           | 1 PBUTN, 1 WBUTN | ART-Pi               | -        | LCD, DVP, RW007 WiFi, TF卡, Buzzer, Audio               |
| hpm6800evk     | HPM6880 | 16MB  | 512MB DDR3 | 1 USB, 1 DBG | 1 RGB           | 2 User           | RPi, ADC 16pin       | 1G       | eMMC, EEPROM, TF卡, Audio, CAN, LCD, MIPI, DVP          |
| hpm6e00evk     | HPM6E80 | 16MB  | 32MB SDRAM | 1 USB, 1 DBG | 1 RGB           | 2 User           | RPi, Motor 32pin     | 1G       | 2 EtherCAT, Audio, ADC, CAN, PPI/FEMC(SDRAM)            |

- Motor 32pin 与 Motor 20pin 兼容
- hpm5300evklite 的 UART to USB 接口芯片 CH340 未焊接
- RPi 表示兼容 [树莓派 GPIO](https://pinout.xyz/)
- [ART-Pi] 是 [RT-Thread] 的一个开源硬件平台，这里表示兼容 [ART-Pi GPIO](https://art-pi.github.io/website/docs/#/tutorial/pin-description)
- ART-Pi 由两个排针座组成, 其中 P1 与树莓派 GPIO 兼容

## 社区资源

### 论坛

- [电子发烧友论坛 - 先楫半导体HPMicro](https://bbs.elecfans.com/group_1700)

### 教程、视频博主和博客作者

- [HPM-FAE - 哔哩哔哩](https://space.bilibili.com/592932589)
- [金探长Jeeed - 哔哩哔哩](https://space.bilibili.com/191119115)
- RCSN
  - [RCSN06 - 哔哩哔哩](https://space.bilibili.com/281444293)
  - 微信公众号：RCSN嵌入式

### 开源项目

- <https://github.com/cherry-embedded/CherryDAP>

## 贡献

欢迎贡献！如果您有任何建议、更正或补充，请随时提出 Issue 或提交 PR.

[hpm-data]: https://github.com/andelf/hpm-data
[ART-Pi]: https://art-pi.github.io/website
[RT-Thread]: https://github.com/RT-Thread/rt-thread
