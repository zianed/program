# USB

Universal Serial Bus 通用串行总线
目的：1994年，统一电脑外设接口标准,实现即插即用。在设备插入时，主机枚举到此设备，并加载所需的驱动程序。


尽可能实现
- 热插拔（Hot plugging）技术
带电插拔，在运行的时候（不关闭电源）进行插拔外设硬件，能够及时侦测和使用新设备。
包含了对软硬件的电源、信号和接地线的接触顺序要求。
支持的接口例如：USB、SATA、SCSI、光纤、PS/2（需要重启）

- 即插即用（PnP, Plug and Play）技术
增加新的外部设备时，能自动侦测与配置硬件资源（如I/O地址、DMA、IRQ），而不需要重新配置或手工安装驱动程序。
支持的接口例如：USB、SCSI、PS/2、IDE、HDMI


## USB功能
USB主要的功能分为三种形式存在，HOST、DEVICE、HUB。

- HOST
作为主机侧存在
Host Controller

  - Universal Host Controller Interface (UHCI): The UHCI specification was initiated by Intel, so your PC is likely to have this controller if it's Intel-based.

  - Open Host Controller Interface (OHCI): The OHCI specification originated from companies such as Compaq and Microsoft. An OHCI-compatible controller has more intelligence built in to hardware than UHCI, so an OHCI HCD is relatively simpler than a UHCI HCD.

  - Enhanced Host Controller Interface (EHCI): This is the host controller that supports high-speed USB 2.0 devices. EHCI controllers usually have either a UHCI or OHCI companion controller to handle slower devices.

  - USB OTG controllers: They are getting increasingly popular in embedded microcontrollers. With OTG support, each communicating end can act as a dual-role device (DRD). By initiating a dialog using the Host Negotiation Protocol (HNP), a DRD can switch itself to host mode or device mode based on the desired functionality.

- DEVICE
作为设备侧存在

- HUB
USB扩展器
通过HUB可以连接到多个外设。分层多级。


function

## USB协议发展
- USB1


- USB2
最大传输速率480Mbps

- USB3
最大传输速率20Gbps
TYPE-A，TPYE-C两种形式接口。

- USB4
最大传输速率40Gbps
兼容DisplayPort和Thunderbolt 3


## USB物理接头
分为
- Type-A，主流使用
- Type-B
- Type-C，主流使用

## Linux上的USB


### uhci


## Windows上的USB
Universal Serial Bus (USB) provides an expandable, hot-pluggable Plug and Play serial interface that ensures a standard, low-cost connection for peripheral devices such as keyboards, mice, joysticks, printers, scanners, storage devices, modems, and video conferencing cameras. 
https://docs.microsoft.com/en-us/windows-hardware/drivers/usbcon/



## USB标准组织
USB开发者论坛 USB Implementers Forum (USB-IF)
http://www.usb.org/home


## 参考资料
Universal Serial Bus
http://embeddedlinux.org.cn/essentiallinuxdevicedrivers/final/ch11lev1sec1.html


