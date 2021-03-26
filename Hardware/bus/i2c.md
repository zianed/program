# I2C总线

## I2C
Inter-Integrated Circuit，集成电路总线，串行通信总线，飞利浦制定。

使用多主从架构，为了让主板等用以连接低速外围设备。

### 结构
使用2条双向漏极开路线，传输数据。
- 一条线为传输数据的串行资料线SDA(Serial Data Line)。
- 一条线是启动或停止传输以及发送时钟序列的串行脉冲线SCL(Serial Clock Line)。

两条线上都有上拉电阻，典型电压为+3.3V或+5V。




## SMBbus


I2C and SMBus Subsystem
https://www.kernel.org/doc/html/latest/driver-api/i2c.html

