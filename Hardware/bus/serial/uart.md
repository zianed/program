UART总线


## UART
Universal Asynchronous Receiver/Transmitter，通用异步接收器/发送器。异步串行总线，没有时钟，一般叫做串口。

UART是异步串行通信口的总称。点对点。
RS232、RS449、RS423、RS422等，是对应各种异步串行通信口的接口标准和总线标准，属于通信网络中的物理层。

COM是PC上异步通信口的简称，IBM的外部接口配置为RS232，成为默认的标准。

传输速度比较慢，一般在115200bps=115Kbps
大部分UART控制器也能支持到4Mbps或者8Mbps

一对一，全双工，传输距离不长。


### 结构
- PC相关的COM口，有9个pin，是RS232电平标准，+15/+13V表示1，-15/-13V表示0。
- 单片机相关的UART口，有4个pin，是TTL电平标准，+5V表示1,0V表示0。


相关概念
- Baud Rate：波特率
- Word Length：一帧数据帧的位数
- Parity：奇偶校验位
- Stop Bits：停止位
- Data Direction：数据方向
- Over Sampling：接受采样

UART通常分为三线和5线：
- 三线：data receive(RX)，data transmit(TX)，ground reference(GND)。

- 五线：增加request to send(RTS)，clear to send(CTS)。做硬件流控，接收端在FIFO缓冲区满的时候，发送端等待发送数据。


### 使用
主要用作调试接口。串口调试打印日志。
外接蓝牙、GPS、Radio等设备。

USART：
Universal Synchronous asynchronous receiver and transmitter通用同步异步收发器
增加同步功能，提供主动时钟
增加同步功能，提供主动时钟


### 参考资料

- UART
https://developer.android.com/things/sdk/pio/uart

- UART: A Hardware Communication Protocol Understanding Universal Asynchronous Receiver/Transmitter
https://www.analog.com/en/analog-dialogue/articles/uart-a-hardware-communication-protocol.html


