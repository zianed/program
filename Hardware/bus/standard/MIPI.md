# MIPI

移动行业处理器接口Mobile Industry Processor Interface
包含一套协议和标准。

The vision of MIPI Alliance is to develop the world's most comprehensive set of interface specifications for mobile and mobile-influenced devices.
The mission of MIPI Alliance is to provide the hardware and software interface specifications device vendors need to create state-of-the-art, innovative mobile-connected devices while accelerating time-to-market and reducing costs.
The organization actively promotes and encourages the adoption of its specifications throughout mobile and mobile-influenced markets.

内部已Group的形式来运作，分为12个Group。


## MIPI协议簇
- MIPI移动系统框图
![MIPI移动系统框图](https://www.mipi.org/sites/default/files/MIPI-Mobile-System-Diagram-June2018.jpg)

- MIPI多媒体声明
![MIPI多媒体声明](https://www.mipi.org/sites/default/files/MIPI_MultimediaSpecifications__Oct17._0.jpg)

MIPI Alliance specifications serve six fundamental application areas: physical layer, multimedia, chip-to-chip or interprocessor communications (IPC), control/data, and debug/trace and software.


六大部分：
- Physical layer—A family of high-speed physical layers to serve essential interconnection needs in a device
- Multimedia—Protocols for camera and imaging, display and touch, and a complete interface for audio
- Chip-to-chip/IPC—Protocol layers for chip-to-chip or interprocessor communications
- Control and data—Interfaces to manage lower-speed components 
- Debug and trace—Tools for debugging embedded systems throughout the development lifecycle
- Software integration—Tools that streamline software integration of components in mobile-connected products


## 主要MIPI协议

### MIPI CSI
MIPI Camera Serial Interface
定义了摄像头和HOST设备之前的接口。CSI可以由C-PHY或者D-PHY实现。

指令操作：
- CCS：Camera Command Set摄像头指令集
控制摄像头设备的常用命令。

类似的传输接口：
CAMIF：Camera Interface


### MIPI DSI
MIPI Display Serial Interface
高速差分信号点对点串行总线。以串行的方式发送像素数据或者指令给LCD等设备。支持高分辨率的显示屏。

包括：
- 一条高速时钟lane，clock lane。
- 一条或者多条数据lane，data lane。

由于是差分信号，每一条lane基于两条线来传输。从HOST设备发向Device设备。lan0可以进行总线周转，因此允许其反转方向。读取设备端的信息和像素等数据。如果使用多个lane，数据中的每个顺序位在下一个通道上传输。
常用的由1-lane，4-lane等。

link操作可以分为lower power(LP)模式和high speed(HS)模式。
在低功耗模式下，高速时钟被禁用，时钟信号被嵌入在数据中传输。

指令操作：
- DCS：Display Command Set显示指令集
控制显示设备的常用命令。

- MCS：Manufacture Command Set制造商指令集
制造商实现

类似的传输接口：
FPD-Link
LVDS：Low-Voltage Differential Signaling低电差分信号
eDP
HDMI


### I3C



## 参考资料
- MIPI Alliance
https://www.mipi.org

- MIPI Alliance About
https://www.mipi.org/about-us

