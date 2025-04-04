# CSAPP

<hr />

针对x86-64

## <a id = "index" >Index:</a>

​	[Bits,Bytes and Integers](#bits)









































#### <span id = "bits"><a href = '#index'>Bits,Bytes and Integers</a></span>

<hr />

主题：数字的位级表示，操作对数字属性的影响， 临界条件。

基础：

- 字长：cpu一次性处理的位数
- long double 占用10/16字节， 在64位机器上16字节保持对齐	
- 虚拟地址空间由机器字长决定，地址值位数
- 位级运算：& ， | ， ~ ， ^(异或)， 可以理解成一种对为一位数集合的运算，
- 逻辑操作符，注意 !0xab = 0x00 !0x00 = 0x01， p&&*p
- 位移操作符：<<, >> ,逻辑位移log.(用零填充)和算术位移Arith.（正数：左右移都补零；负数左移右补0左补1；右移左补1）
- 位移大于位数的位移会先模位数再位移

- unsigned 和 signed 比较时：当两边存在一个unsigned（末尾加U）时，会将signed变成unsigned
- 有符号数Tmin的相反数还是自己 ，Tmin =  -(Tmax) - 1 ; 相同位的无符号数Umax = 2（Tmax）+ 1
- 当循环索引被设置为unsigned时，边界为0/Umax，循环可能一直执行
- sizeof返回unsigned值

​	拓展

： 无符号数删位相当于模剩下位数的十进制；



​	



