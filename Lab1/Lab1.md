### Lab1

**阅读Chapter2/4.3/4.4；**

```
开机初始化，运行ROM中的BootLoader，将xv6的内核加载到内存0x80000000中，CPU从kernel/entry.S的_entry出发执行，分配一个CPU的栈的大小; 跳转到start.c中的start函数，进行机器模式下的初始化配置，跳转到main函数。main函数对设备和子系统进行初始化，包括第一个用户进程的创建。
```

**User-space code in user/user.h && user/usys.pl**

```
user.h: 主要是一些系统调用函数和用户常用函数的接口
uses.pl: 系统调用的入口
```

**Kernel-space code in kernel/syscall.h && kernel/syscall.c**

```
syscall.h: 给定系统调用号
syscall.c: 进行系统调用
```

**Process-related code in kernel/proc.h && kernel/proc.c**

```
proc.h: context/cpu/trapframe/proc结构体的定义
				context: 内核进程切换时需要保存的上下文
				cpu: 记录cpu的状态——管理的进程+上下文+push_off() depth??? +interrupt enable
				trapframe: 用于保存在用户态和内核态切换时的一些信息
				proc: 记录每个进程的状态，包括——锁+状态+父进程+上下文+文件描述表...
proc.c: 进程相关的函数
				procinit: 是在boot时初始化进程列表
				allocproc: 在进程表找不再使用的proc struct或者new一个新的proc struct
```





##### 实验工作总结



##### 遇到的困难以及收获

##### 对课程或Lab的意见和建议

##### 参考文献