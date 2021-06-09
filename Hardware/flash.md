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


# eMMC，
基于Nand flash技术开发的


# UFS，Universal Flash Storage
UFS目标是发展一套统一的快闪存储卡格式，提高数据传输的速度和稳定性。
UFS使用MIPI的M-PHY物理层进行开发。并行信号改串行信号，半双工改全双工。
UFS实现全双工的LVDS串口，较8个平行线程的eMMC拥有更宽的带宽。


# 参考资料
- Universal Flash Storage (UFS)
https://www.jedec.org/standards-documents/focus/flash/universal-flash-storage-ufs


