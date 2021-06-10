# 闪存 Flash memory
允许在操作中被多次擦或者写的存储器。是一种特殊的、以宏块抹写的EEPROM。


## Nor Flash
随机存取外部地址总线。从Nor Flash读取资料的方式与从RAM读取资料相近。存储在Nor Flash上的程序不需要复制到RAM就可以直接运行。
写入Nor Flash单元的动作可以单一字节的方式进行。
最常见用途是BIOS ROM芯片。

### SPI Nor Flash
串行

### CFI Nor Flash
并行


## Nand Flash
相比Nor Flash具有较高的存储密度和较低的每比特成本。
读取和写入的动作以“页”位单位偏移量进行，抹除动作只能以“区块”为单位偏移量进行。


### Nand Flash


### SPI Nand Flash


# eMMC，embeded MultiMedia Card，嵌入式多媒体卡
基于Nand flash技术开发。
将MMC组件放入一个小的球栅数组封装中，印刷在电路板上。


# UFS，Universal Flash Storage
UFS目标是发展一套统一的快闪存储卡格式，提高数据传输的速度和稳定性。
UFS使用MIPI的M-PHY物理层进行开发。并行信号改串行信号，半双工改全双工。
UFS实现全双工的LVDS串口，较8个平行线程的eMMC拥有更宽的带宽。



# Memory Card，存储卡
使用Flash芯片作为储存介质。

分类：
- Secure Digital(SD Card)
- U盘(USB flash)
- 


# CMSIS标准驱动对存储暴露的接口

- Memory Card Interface
SD/MMC Memory

implements the hardware abstraction layer for Secure Digital (SD) and Multi Media Card (MMC) memory that is typically used as file storage. For embedded systems, SD/MMC devices are available as memory cards in several forms (SD, miniSD, microSD, MMC, MMCmicro) or as non-removable devicees that are directly soldered to the PCB (eMMC).

The MCI driver allows you to exchange data of the SD/MMC memory via SD/MMC interface.

The following modes are supported by SD/MMC memory cards:
SPI bus mode: Serial Peripheral Interface Bus supported by most microcontrollers.
1-bit SD/MMC Bus mode: proprietary data transfer protocol supported by SD/MMC interfaces.
4-bit SD/MMC Bus mode: high-speed version of the SD/MMC interface using 4 data I/O pins.
8-bit SD/MMC Bus mode: high-speed version of the SD/MMC interface using 8 data I/O pins.

https://arm-software.github.io/CMSIS_5/latest/Driver/html/group__mci__interface__gr.html

- Flash Device Interface
NOR Flash memory

The Flash API provides a generic API suitable for Flashes with NOR memory cells independent from the actual interface to the MCU (memory bus, SPI, ...). SPI flashes are typically not named NOR flashes but have usually same flash cell properties.
https://arm-software.github.io/CMSIS_5/latest/Driver/html/group__flash__interface__gr.html

- NAND Flash Device Interface
NAND Flash memory

NAND Flash is organized in pages, grouped into blocks as the smallest erasable unit.
https://arm-software.github.io/CMSIS_5/latest/Driver/html/group__nand__interface__gr.html

- Storage Device Interface

This is an abstraction for a storage controller. It offers an interface to access an address space of storage locations, comprising APIs for initialization, erase, access, program, and status-fetch operations. 
https://arm-software.github.io/CMSIS_5/latest/Driver/html/group__storage__interface__gr.html


# 参考资料
- Universal Flash Storage (UFS)
https://www.jedec.org/standards-documents/focus/flash/universal-flash-storage-ufs


