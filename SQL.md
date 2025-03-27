## SQL

关系数据库：

​	数据类型：

​			

|               |                |                                   |
| ------------- | -------------- | --------------------------------- |
| INT           |                |                                   |
| BIGINT        |                |                                   |
| REAL/FLOAT(N) |                |                                   |
| DOUBLE        |                |                                   |
| DECIMAL(M, N) |                | 用户指定精度，M:位数， N:小数位数 |
| CHAR(N)       |                | 指定长度字符串                    |
| VARCHAR(N)    |                | 可变长度字符串                    |
| BOOLEAN       |                |                                   |
| DATE          | 日期类型       |                                   |
| TIME          | 时间类型       |                                   |
| DATEITME      | 日期和时间类型 |                                   |

SQL语言是各数据库之间通用，可操作数据库

DDL：允许用户定义数据，也就是创建表、删除表、修改表结构

DML：允许用户添加、删除、更新数据

DQL：允许用户查询数据



关键字大写，表名列名小写



MySQL

​	实际上是一个接口，内部包含多种引擎InnoDB、MySAM







mysql9.2.0手动安装常见问题：

​	1.命令行请用管理员权限访问

​	2.安装需配置my.ini文件，新创建data文件夹

```html
<!--需要配置参数为
[mysqld]
port端口号3306 
basedir安装目录
datadir数据存放目录
max_connections允许最大连接数200
max_connect_errors允许连接失败的次数10
character-set-server字符集utf8mb4
default-storage-engine新表的默认存储引擎
！！！my_native_password在8.4版本后默认已不安装！！！
！！！使用caching_sha2_password插件-->
<a href = 'https://www.tubring.cn/articles/fix-php-mysql-84-mysql_native_password-not-loaded'>具体说明</a>


<!--[mysql]
default-character-set = utf8mb4
[client]
port = 3306
default-character-set = utf8mb4-->
```



首次安装部署服务器和服务，先使用管理员权限访问cmd，将路径设置到bin包下

```python
$mysqld --initialize --console #记录临时密码
```

```python
$mysqld install  #安装服务
```

启动服务

```python
$net start mysql
```



登录数据库

```python
$mysql -u root -p
```



修改密码

```python
$mysql> ALTER USER 'root'@'localhost' IDENTIFIED WITH caching_sha2_password BY '[]' ; #[]为密码
$mysql> FLUSH PRIVILEGES;
```



退出

```python
$mysql>quit;
```

