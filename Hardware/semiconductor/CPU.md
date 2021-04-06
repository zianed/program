CPU

# 中央处理器


| 分类 | 英文 | 名称 | 含义 | 备注 |
| --- | --- | --- | --- | --- |
| CPU | Central Processing Unit | 中央处理单元 | 做通用计算。 |  |
| GPU | Graphics Processing Unit | 图形处理单元 | 做图形处理计算，图形加速。 | 渲染 |
| NPU | Neural Network Processing Unit | 神经网络处理单元 | 做人工智能计算。 | |


# 指令架构集

常见指令集架构（Instruction Set Architecture, ISA）

| 分类 | 英文 | 名称 | 含义 | 
| --- | --- | --- | --- |
| CISC | Complex Instruction Set Computing | 复杂指令运算 | x86架构，x86-64架构 |
| RISC | Reduced Instruction Set Computing | 精简指令运算 | PowerPC，MIPS，SPARC，ARM |
| EPIC | Explicitly Parallel Instruction Computing | 显示并发指令运算 | 允许根据编译器的调度并执行指令，ia64 |
| VLIW | Very Long Instruction Word | 超长指令字 | 利用指令集并行优势 |

## 常见RIC指令集

- ARM：Advanced RISC Machine 
https://www.arm.com

- RISC-V：开源指令架构集，小型快速低功耗，始于伯克利大学
https://riscv.org/

- MIPS：Microprocessor without Interlocked Pipeline Stages，无互锁流水线微机
https://www.mips.com/

- PowerPC：Performance Optimized With Enhanced RISC Performance Computing 
https://openpowerfoundation.org/

- SPARC：Scalable Processor Architecture 
https://sparc.org/



# CPU指标

CPU cache的一个重要标准就是L1 cache的Load-to-use laeency，L2/L3 cache的要求是在提供数据的同时尽可能避免 Bus Traffic。


 