GPIO控制


## GPIO
General-purpose input/output，通用型输入输出，引脚可以供使用者自由控制。
A GPIO is a signal pin on an integrated circuit or board that can be used to perform digital input or output functions.

用来连接微处理器和其他电子设备。

PIN脚可以作为输入、输出或输入与输出，如作为clk generator、chip select等。
可以通过引脚输出高低电平或者读入引脚的状态-是高电平或是低电平。


### 结构
GPIO具有更低的功率损耗(大约1µA）。
GPIO器件提供最小的封装尺寸。

GPIO的常用功能：
- Being configurable in software to be input or output
- Being enabled or disabled
- Setting the value of a digital output
- Reading the value of a digital output
- Generating an interrupt when the input changes value


### 使用
最基本的输入功能是检测外部输入电平，如把GPIO引脚连接到按键，通过电平高低区分按键是否被按下。
可以通过GPIO口和硬件进行数据交互(如UART)，控制硬件工作(如LED、蜂鸣器等),读取硬件的工作状态信号（如中断信号）等。

对于LED灯的场景，硬件寄存器可以理解为一个电子开关。
需要亮灯的时候调用GPIO口拉高的函数，需要熄灯的时候调用GPIO拉低的函数，实现控制。函数的操作，最终变成了向GPIO的硬件寄存器写入数据，硬件的状态会跟随寄存器的数据改变而改变。

连接sensor、lcd。
做ADC转换。
做中断处理。

使用很灵活，例如树莓派上的GPIO引脚。
利用GPIO输出PWM信号。
实现I2C、SPI总线。


### 参考资料
- General Purpose Input/Output (GPIO)
http://kernel.org/doc/html/latest/driver-api/gpio

- An Introduction to GPIO Programming
https://www.ics.com/blog/introduction-gpio-programming

- General Purpose Input/Output (GPIO)
https://www.egr.msu.edu/classes/ece480/capstone/fall09/group03/AN_balachandran.pdf
