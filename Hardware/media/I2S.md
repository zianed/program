# I2S总线

## I2S
Intergrated Interchip Sound，在IC间传输数字音频的一种接口标准，由飞利浦半导体制定。常被使用在发送PCM数据的DAC中。
双声道音频数据流


## PCM
Pulse-code modulation，脉冲编码调制，模拟信号的数字化方法。
PCM将信号的强度依照同样的间距分成数段，然后用独特的数字记号来量化。
PCM编码以一种串行通信的形式运作。是一种没有经过压缩的原始的采样数据。


### 结构

典型的I2S至少由三条传输线组成，是同步串行接口。
+ BCLK：bit Clock line，SCK（Serial Clock），连续串行时钟，比特时钟，主设备发出；
+ LRCLK：left-right clock，FS（Frame Select），WS（Word Select），字符选择时钟，左右时钟；0表示左频道，1表示右频道；主设备发出；
+ SDATA：multiplexed data，SD（Serial Data），串行数据线。


以44.1KHz的采用率来说明，允许两个轨道同时发送数据，每个轨道可传输32位数据，则传输它所需要的连续串行时钟为2.8224MHz。
SCK Frequency = SampleRate x BitsPerChannel x numberOfChannels
44.1KHz * 32位 * 2个声道 = 2.8224MHz = 2.8224MBit/s

48KHz * 16bit = 1.536MBit/s
96KHz * 24bit = 4.608MBit/s

I2S is an efficient, straightforward serial-communication protocol that is great for digitized audio. 
专门设计用来传输音频数据。


### 使用
常见的接外围的CodeC、SmartPA等设备


### 参考资料
- I2S bus specification
https://www.sparkfun.com/datasheets/BreakoutBoards/I2SBUS.pdf

- Introduction to the I2S Interface
https://www.allaboutcircuits.com/technical-articles/introduction-to-the-i2s-interface/
