# PCIe

## PCIe
Peripheral Component Interconnect Express
沿用现有的PCI编程概念和信号标准，构建了更加高速的串行通信系统标准。

PCIe拥有更快的速率，能够支持热插拔和热交换特性，支持三种电压+3.3V、3.3Vaux、+12V。
PCIe 6.0可以达到64GT/s的速率。

PCIe主要是为提升电脑内部所有总线的速度。
内置或安装在扩展卡槽上。PCI bus成为了电脑上的标准扩展总线。


## 结构
PCIe创建在点对点的连接lane的基础之上。由多层协议组成。
- 物理层：低电压差分信号，支持x通道连接
- 数据链路层：循环冗余校验
- 事务层：数据提交和应答时间上分离
- 引脚

## 使用
网卡、显卡、声卡，NVMe固态硬盘等都使用PCIe。


## 标准
由PCI-SIG（Peripheral Component Interconnect Sepcial Interest  Group周边元件互连特别兴趣小组）组织制定和维护。
负责制定PIC、PCI-X、PCIe电脑总线规格的电子工业联盟。


### 参考资料
- 深入PCI与PCIe之一：硬件篇
https://zhuanlan.zhihu.com/p/26172972

