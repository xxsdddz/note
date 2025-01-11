# CPU(中央处理器)

组成：RAM，4个寄存器，Control Unit

#### **Control Unit**：

​	指令寄存器（IR）与指令地址寄存器（IAR），与RAM，Registers, ALU相连

程序通过以指令存储在内存中，前4位opcode（操作码），后四位ADDRESS OR REGISTERS。



![](C:\Users\zzp\Pictures\Screenshots\屏幕截图 2025-01-03 110001.png)

时钟向Control Unit提供周期电信号



#### **时钟速度**

```HTML
<p>时钟速度为 3.2 GHz 的 CPU 每秒执行 32 亿个周期。（较早的 CPU 的速度以兆赫计算，或每秒几百万个周期。）</p>
<p>有时，多个指令可在一个时钟周期内完成；而在其他情况下，一条指令可能需要多个时钟周期来处理。由于不同的 CPU 设计处理指令的方式不同，所以最好比较同一品牌和同一代 CPU 的时钟速度</p>
													------intel
```



## **机器指令：**

​	格式：|操作码（opcode）|地址码|寻址方式| （依据cpu处理格式不同）

#### 操作码：

​	固定字长：执行速度快、精简、RISC架构下（常用于嵌入式与移动设备，如：ARM架构、UNIX、Linux、iOS、Android…）



​	可变指令长度：CISC架构、功能齐全（某些软件手机和电脑无法兼容原因：指令集架构不同，如：x86架构（Windows、macOS、linux、部分UNIX）、64位拓展系统）

1.不允许短op码是长op码的前缀（）

2.使用频率高的指令分配短op码



#### 地址码：

根据地址个数（分为四地址指令、三地址指令……）

四地址：

OP | A1 | A2 | A3| A4

​	*A1：第一操作数  A2:第二操作数*

​	*A3：结果 			A4:下条指令地址*

4次访存



（施工中）

//





//



## **缓存**（cache）：

CACHE位于芯片中，空间大小一般为KB和MB。提高数据存取速度，临时保存一些中间值。

解决从内存中读取数据（一个时钟周期）的延迟问题，cpu空等问题

缓存命中（CACHE HIT）：想要数据已经在缓存中

缓存命中（CACHE MISS）：想要数据不在缓存中



脏位

因为存在缓存的数据需要和RAM记录同步，缓存每块空间有一个DIRTY BIT

同步：缓存满了CPU需要新缓存数据时，检查DIRTY BIT，dirty—>写回RAM



### instruction pipelining：

**hazards**：

​	1数据处理冲突：多指令同时对数据进行操作，解决：<u>乱序排序</u>

​	2.控制冲突：分支指令造成空等问题：条件跳转改变程序执行流，造成空等—><u>推测执行</u>（speculative execution）pipelining flush：分支预测（branch prediction）错误

​	3.结构冲突：硬件资源满足不了指令重叠执行的要求



超标量处理器（superscalar）：执行出现频次高的指令（多ALU）



同时运行多个指令流：

多核可共享数据/多cpu（服务器）
