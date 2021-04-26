# SPI总线

## SPI
Serial Peripheral Interface，串行外设总线，首先由摩托罗拉制定。低速同步总线，传输速率比I2C高。

使用全双工模式通信，是一个主从模式。
在每个SPI时钟周期内，都会发生全双工数据传输。主设备在MOSI线上发送一个位，从设备读取；同时从机在MISO上发送一位数据，主机读取。即使只有单向数据传输，工作方式仍然是双工的。

主机负责初始化帧，数据帧可用于读写操作，片选线路可以从多个从机选择一个来响应主机的请求。

### 结构

SPI是四线接口，是同步串行接口。
+ SCLK：Serial Clock，串行时钟，由主机发出；
+ MOSI：Master Output Slave Input，主机输出从机输入信号，由主机发出；
+ MISO：Master Input Slave Output，主机输入从机输出信号，由从机发出；
+ SS：Slave Select，片选信号，由主机发出。


全双工通信，传输速率可达10Mbps水平，比I2C快。
需要的接口比I2C多。
SPI的从设备是通过片选线来区分的，I2C的从设备是通过地址来区分的。SPI总线每多挂一个从设备，就需要多用一个线作为片选线。
I2C总线的管脚都是开漏输出，必须外接上拉电阻。


### 使用
常见的接外围的小尺寸lcd、sensor等设备


### 参考资料

- Introduction to I²C and SPI protocols
https://www.byteparadigm.com/applications/introduction-to-i2c-and-spi-protocols/

