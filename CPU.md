# CPU(中央处理器)

组成：RAM，4个寄存器，Control Unit

**Control Unit**：

​	指令寄存器（IR）与指令地址寄存器（IAR），与RAM，Registers, ALU相连

程序通过以指令存储在内存中，前4位opcode（操作码），后四位ADDRESS OR REGISTERS。

一个指令：fetch-decode-excute 之后IAR+1继续执行

![](C:\Users\zzp\Pictures\Screenshots\屏幕截图 2025-01-03 110001.png)

时钟向Control Unit提供周期电信号



**时钟速度**

```HTML
<p>时钟速度为 3.2 GHz 的 CPU 每秒执行 32 亿个周期。（较早的 CPU 的速度以兆赫计算，或每秒几百万个周期。）</p>
<p>有时，多个指令可在一个时钟周期内完成；而在其他情况下，一条指令可能需要多个时钟周期来处理。由于不同的 CPU 设计处理指令的方式不同，所以最好比较同一品牌和同一代 CPU 的时钟速度</p>
													------intel
```