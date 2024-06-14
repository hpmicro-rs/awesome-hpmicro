# Awesome HPMicro

An unofficial curated list of HPMicro MCU related code and resources.

## Official Resources

- Homepage: [先楫半导体 HPMicro](https://www.hpmicro.com/)
  - Datasheet, User Manual, Errata, Design Guide, KiCAD Footprint: [设计资源/芯片资料](https://www.hpmicro.com/resources/resources.html)
  - Forum: [先楫社区](https://www.hpmicro.com/support/forumpark.html)
- Online Shop: [在线购买](https://www.hpmicro.com/support/shop.html)
- All-in-one Resources on Baidu Netdisk: [百度网盘](https://pan.baidu.com/s/1RaYHOD7xk7fnotmgLpoAlA?pwd=xk2n)
- [Pinmux Tool](https://tools.hpmicro.com/pinmux)
- [Bilibili - 先楫半导体HPMicro](https://space.bilibili.com/1306310554)

### Official Repositories

- GitHub Organization: [GitHub - hpmicro](https://github.com/hpmicro)
- Gitee Mirror: [Official mirror of HPMicro](https://gitee.com/hpmicro)
- Official SDK: [hpm_sdk](https://github.com/hpmicro/hpm_sdk)
  - HPM SDK Documentation: [HPM SDK 文档](https://hpm-sdk.readthedocs.io/zh-cn/latest/)
- HPMicro Manufacturing Tool: [hpm_manufacturing_tool](https://github.com/hpmicro/hpm_manufacturing_tool)
- OpenOCD Fork: [hpmicro/riscv-openocd](https://github.com/hpmicro/riscv-openocd)
  - The corresponding configuration files are located in `hpm_sdk/boards/openocd/`
- VSCode Extension: [hpm_pinmux_tool](https://github.com/hpmicro/hpm_pinmux_tool) - No update since September 27, 2023, use the Pinmux tool instead.

### Third-party RTOS Support

- Zephyr: [zephyrproject-rtos/hal_hpmicro](https://github.com/zephyrproject-rtos/hal_hpmicro)
- NuttX: [hpmicro/nuttx_apps](https://github.com/hpmicro/nuttx_apps)
- RT-Thread: [RT-Thread/rt-thread/bsp/hpmicro](https://github.com/RT-Thread/rt-thread/tree/master/bsp/hpmicro)

### IDE Support

- [SEGGER Embedded Studio for RISC-V](https://www.segger.com/downloads/embedded-studio/#ESforRISCV)
  - License application for HPMicro: <https://license.segger.com/hpmicro.cgi>

## IP Cores

The RISC-V IP cores are provided by Andes Technology Corporation.

- [Andes Product Documentation](http://www.andestech.com/en/products-solutions/product-documentation/)
  - The IP cores used by HPMicro are D25(F)(for HPM5xxx) and D45(for HPM6xxx)

The M_CAN IP core is provided by Bosch.

- Intro and documentation [M_CAN - Bosch](https://www.bosch-semiconductors.com/ip-modules/can-ip-modules/m-can/)

## Dev Boards

- hpm5300evk
- hpm5301evklite
- hpm6200evk
- hpm6300evk
- hpm6750evk
- hpm6750evk2
- hpm6750evkmini
- hpm6800evk

## Contributing

Contributions are welcome! If you have any suggestions, corrections, or additions, please feel free to open an issue or submit a pull request.
