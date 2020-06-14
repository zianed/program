# IPC 进程间通信 Inter-Process Communication
在不同进程间通信，交换数据。

+ signal 信号


+ pipe 管道



+ fifo 命名管道


+ shared memory 共享内存
两个不相关的进程访问同一块逻辑内存。
#include <sys/shm.h>

| 函数名 | 函数含义 | 备注 |
| --- | --- | --- |
| shmget | 创建共享内存 | |
| shmat | 启动对共享内存的访问 | |
| shmdt | 分离对共享内存的访问 | |
| shmctl | 控制共享内存 | |


+ message queue 消息队列
从一个进程向另一个进程发送数据块。
#include <sys/types.h>
#include <sys/ipc.h>
#include <sys/msg.h>

msgget
msgsend
msgrcv
msgctl

使用同一个key作为两个进程之间的关键字。


+ socket 套接字
socket pair作为




+ 工具
使用ipcs命令查看系统当前IPC通道信息