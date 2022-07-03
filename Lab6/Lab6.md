### Lab6

进程切换的方式：

​	调度器和其他进程之间反复切换，kernel/proc.c中，sched会从当前进程切换到调度器，scheduler从调度器切换到一个runnable的进程，swtch(.S)函数进行上下文的切换（注意ra也是被保存和切换的）

​	p->lock保证CPU和进程运行的正确性；在使用mycpu时要确保中断禁止

生产者消费者 & sleep/wakeup机制（kernel/proc.c sleep wakeup函数）

管道的实现PIPE（kernel/pipe.c pipewrite piperead）：环形缓冲区

kernel/pipe.c 中的exit/wait/kill

​	