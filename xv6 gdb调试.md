### xv6 gdb调试

1. ![截屏2021-10-12 下午9.42.39](/Users/bettywu/Library/Application Support/typora-user-images/截屏2021-10-12 下午9.42.39.png)

以上的报错需要新建一个~/.gdbinit文件并且写入 

```
set auto-load safe-path
```

2. 接下来<img src="/Users/bettywu/Library/Application Support/typora-user-images/截屏2021-10-12 下午9.43.54.png" alt="截屏2021-10-12 下午9.43.54" style="zoom:50%;" />提示我们架构不同，所以使用

```
gdb-multiarch
```

​	自主选择对应的架构

3. 一些常用的gdb指令

```
info sources // 给出定义的程序
info functions // 列出所有的函数
b kernel/main.c 13 // 在对应文件的第13行打断点
c	// 运行continue
s xx // 运行xx次
bt // backtrace可以打印出栈中的函数
help info // 可以得到info指令可以使用的方式
```

