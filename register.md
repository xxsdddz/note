# **寄存器&内存**

**锁存器（latch）：**

​	保存一位二级制码，寄存器的单元，数据输入线与允许写入线。

**寄存器（register）：**

​	width: 位宽

​	锁存器**矩阵**组成，行线与列线（启用对应锁存器）

​	一根允许写入线，一根允许输出线，（m）根行线，（n）根列线，一根输出输入线

**多路复用器**（Multiplexer）：

​	解码8位地址，将address对应的行列线接通 

**256-BIT MEMORY**：

​	8位地址（16行*16列，2^4 = 16，行列分别用4位二进制码表示）

**RAM（随机存取存储器）**：

由MEMORY并列排放，断电数据消失

**SRAM：静态随机存取存储器**

