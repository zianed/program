# I2C总线

## I2C
Inter-Integrated Circuit，集成电路总线，串行通信总线，首先由飞利浦制定。低速总线。

半双工，只有2根线。

使用多主从架构，为了让主板等用以连接低速外围设备。


### 结构
使用2条双向漏极开路线，传输数据。
- 一条线为传输数据的串行资料线SDA(Serial Data Line)，数据线。
- 一条线是启动或停止传输以及发送时钟序列的串行脉冲线SCL(Serial Clock Line)，时钟线。

两条线上都有上拉电阻，典型电压为+3.3V或+5V。

使用7位或10位地址空间。保留了16个地址，一组总线最多可以和128-16=112个节点通信。最大节点数也会受制于总电容，一般为400pF。
- 常见的I2C总线传输速度标准模式100kbit/s，低速模式10kbit/s。
- 新一代I2C总线传输速度快速模式400kbit/s，高速模式5Mbit/s。


### 使用
常见的接外围的sensor、tp等设备


### 参考资料
- I2C-bus specification and user manual
https://www.nxp.com/docs/en/user-guide/UM10204.pdf

- I2C-Bus
https://www.i2c-bus.org/

- I2C overview
https://wiki.stmicroelectronics.cn/stm32mpu/wiki/I2C_overview


## SMBbus

System Management Bus

The main application of the SMBus is to monitor critical parameters on PC motherboards and in embedded systems.

I2C and SMBus Subsystem
https://www.kernel.org/doc/html/latest/driver-api/i2c.html


## Linux I2C驱动

Linux中可以把I2C设备当做普通字符设备来处理，另一种是利用Linux的I2C驱动体现架构来处理。

分为2部分：
I2C总线驱动，SoC硬件接口，i2c_adapter；
I2C设备驱动，对设备端的实现，i2c_driver。

主要的操作，选定总线号，读写传输数据。

