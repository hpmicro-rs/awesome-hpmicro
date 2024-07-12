# Awesome HPMicro

An unofficial curated list of HPMicro MCU related code and resources.

## Official Resources

- Homepage: [先楫半导体 HPMicro](https://www.hpmicro.com/)
  - Datasheet, User Manual, Errata, Design Guide, KiCAD Footprint: [设计资源/芯片资料](https://www.hpmicro.com/resources/resources.html)
  - Forum: [先楫社区](https://www.hpmicro.com/support/forumpark.html)
- Online Shop: [在线购买](https://www.hpmicro.com/support/shop.html)
- **All-in-one Resources on Baidu Netdisk**: [百度网盘](https://pan.baidu.com/s/1RaYHOD7xk7fnotmgLpoAlA?pwd=xk2n)
- [Pinmux Tool](https://tools.hpmicro.com/pinmux)
- [Bilibili - 先楫半导体HPMicro](https://space.bilibili.com/1306310554)
- WeChat Official: 先楫半导体HPMicro

### Official Repositories

- GitHub Organization: [GitHub - hpmicro](https://github.com/hpmicro)
- Gitee Mirror: [Official mirror of HPMicro](https://gitee.com/hpmicro)
- **Official SDK**: [hpmicro/hpm_sdk](https://github.com/hpmicro/hpm_sdk)
  - HPM SDK Documentation(zh-cn): [HPM SDK 文档](https://hpm-sdk.readthedocs.io/zh-cn/latest/)
  - HPM SDK Documentation(en): [HPM SDK Documentation](http://doc.hpmicro.com/sdk_doc/en/latest/html/index.html)
- Arduino Support: [hpmicro/arduino](https://github.com/hpmicro/arduino)
- HPMicro Manufacturing Tool: [hpm_manufacturing_tool](https://github.com/hpmicro/hpm_manufacturing_tool)
- OpenOCD Fork: [hpmicro/riscv-openocd](https://github.com/hpmicro/riscv-openocd)
  - The corresponding configuration files are located in `hpm_sdk/boards/openocd/`
- VSCode Extension: [hpm_pinmux_tool](https://github.com/hpmicro/hpm_pinmux_tool) - No update since September 27, 2023, use the Pinmux tool instead.

### Third-party RTOS Support

- Zephyr: [zephyrproject-rtos/hal_hpmicro](https://github.com/zephyrproject-rtos/hal_hpmicro)
- NuttX: [hpmicro/nuttx](https://github.com/hpmicro/nuttx)
  - [hpmicro/nuttx_apps](https://github.com/hpmicro/nuttx_apps)
- RT-Thread: [RT-Thread/rt-thread/bsp/hpmicro](https://github.com/RT-Thread/rt-thread/tree/master/bsp/hpmicro)

### IDE Support

- [SEGGER Embedded Studio for RISC-V and ARM](https://www.segger.com/downloads/embedded-studio/#embeddedstudio)
  - License application for HPMicro: <https://license.segger.com/hpmicro.cgi>

## IP Cores

The RISC-V IP cores are provided by Andes Technology Corporation.

- [Andes Product Documentation](http://www.andestech.com/en/products-solutions/product-documentation/)
  - The IP cores used by HPMicro are D25(F)(for HPM5xxx) and D45(for HPM6xxx)

The M_CAN IP core is provided by Bosch.

- Intro and documentation [M_CAN - Bosch](https://www.bosch-semiconductors.com/ip-modules/can-ip-modules/m-can/)

The EtherCAT Slave Controller IP core is provided by Beckhoff Automation.

- PDF [Section I – Technology](https://download.beckhoff.com/download/document/io/ethercat-development-products/ethercat_esc_datasheet_sec1_technology_2i3.pdf)
- PDF [Section II - Register Description](https://download.beckhoff.com/download/document/io/ethercat-development-products/ethercat_esc_datasheet_sec2_registers_3i0.pdf)

## Chip Families

Refer: [hpm-data]

## Dev Boards

| Board          | MCU     | Flash | Ext Memory | USB          | User LEDs       | User Buttons     | GPIOs                | Ethernet | Extra                                                   |
|----------------|---------|-------|------------|--------------|-----------------|------------------|----------------------|----------|---------------------------------------------------------|
| hpm5300evklite | HPM5301 | 1MB   | -          | 1 USB, 1 UART| 1 Red           | 1 Boot, 1 User   | RPi                  | -        |                                                         |
| hpm5300evk     | HPM5361 | 1MB   | -          | 1 USB, 1 DBG | 1 Red           | 1 User, 1 WBUTN  | RPi, Motor 32pin     | -        | ADC, CAN, LIN, 485, 422                                 |
| hpm6200evk     | HPM6280 | 16MB  | -          | 1 USB, 1 DBG | 1 RGB           | 1 PBUTN          | ART-Pi, Motor 20pin  | -        | ADC, HRPWM                                              |
| hpm6300evk     | HPM6360 | 16MB  | 32MB SDRAM | 1 USB, 1 DBG | 1 Green         | 1 PBUTN, 1 WBUTN | RPi, Motor 20pin     | 100M     | TFCard, CAN                                             |
| hpm6750evk     | HPM6750 | 16MB  | 32MB SDRAM | 2 USB, 1 DBG | 1 RGB           | 1 PBUTN, 1 WBUTN | 12pin, Motor 20pin   | 1G, 100M | LCD/TP, DVP, TFCard, CAN, Audio, Buzzer                 |
| hpm6750evk2    | HPM6750 | 16MB  | 32MB SDRAM | 2 USB, 1 UART| 1 RGB           | 1 PBUTN, 1 WBUTN | 12pin, Motor 20pin   | 1G, 100M | LCD/TP, DVP, TFCard, CAN, Audio                         |
| hpm6750evkmini | HPM6750 | 8MB   | 16MB SDRAM | 1 USB, 1 DBG | 1 RGB           | 1 PBUTN, 1 WBUTN | ART-Pi               | -        | LCD, DVP, RW007 WiFi, TFCard, Buzzer, Audio             |
| hpm6800evk     | HPM6880 | 16MB  | 512MB DDR3 | 1 USB, 1 DBG | 1 RGB           | 2 User           | RPi, ADC 16pin       | 1G       | eMMC, EEPROM, TFCard, Audio, CAN, LCD, MIPI, DVP        |
| hpm6e00evk     | HPM6E80 | 16MB  | 32MB SDRAM | 1 USB, 1 DBG | 1 RGB           | 2 User           | RPi, Motor 32pin     | 1G       | 2 EtherCAT, Audio, ADC, CAN, PPI/FEMC(SDRAM)            |

- Motor 32pin is compatible with Motor 20pin
- UART to USB chip CH340 for hpm5300evklite is unsoldered
- [RPi] means [Raspberry Pi GPIO header compatible](https://pinout.xyz/)
- [ART-Pi] is an open-source hardware platform for [RT-Thread], here it means [ART-Pi GPIO header compatible](https://art-pi.github.io/website/docs/#/tutorial/pin-description).
- The P1 header of ART-Pi is compatible with RPi GPIO header

## Community Resources

### Forums

- ElecFans BBS [电子发烧友论坛 - 先楫半导体HPMicro](https://bbs.elecfans.com/group_1700)

### Tutorials, Vlogger, and Bloggers

- [HPM-FAE - Bilibili](https://space.bilibili.com/592932589)
- [金探长Jeeed - Bilibili](https://space.bilibili.com/191119115)
- RCSN
  - [RCSN06 - Bilibili](https://space.bilibili.com/281444293)
  - WeChat Official Account: RCSN嵌入式

### Built with HPMicro

Awesome Projects:

- <https://github.com/cherry-embedded/CherryDAP>

## Contributing

Contributions are welcome! If you have any suggestions, corrections, or additions, please feel free to open an issue or submit a pull request.

[hpm-data]: https://github.com/andelf/hpm-data
[ART-Pi]: https://art-pi.github.io/website
[RT-Thread]: https://github.com/RT-Thread/rt-thread
