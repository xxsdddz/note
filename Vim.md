# Vim

文本编辑器

h :左移  j:下移  k:上移  l:右移

x:删除光标处字符

:q!  :退出编辑器并不保存修改

:wq :退出并保存修改

正常模式下a:进入光标后插入模式

正常模式下i:进入光标后插入模式

正常模式下v:视图模式



operator [number] motion



d [number]  motion-------删除命令

dw 删除到下个单词起始

de 删除到单词末尾

dd 删除整行

d$ 删除光标到句尾

dd:剪切并复制，p粘贴到光标下一行

2w:光标向前移动到两个单词开头

2e:光标向前移动到两个单词末尾

0:行首  $:行末

u:撤销  ctrl+r :redo被撤销的命令



c [number] motion

清除并进入插入模式



r替换光标字符



/string 查找字符串 n下一个 N上一个

？string反向

%跳到配对的符号处（}、]、)、>）



[row] G 跳转到第几行

G 跳转末尾

gg 跳转开头



:s/old/new            替换该行第一个匹配字符串

:s/old/new/g		替换该行所有匹配字符串	

:%s/old/new/g		替换全文匹配字符串

:%s/old/new/gc  	替换全文匹配字符串并请求确认



:![command]			执行外部shell命令

:w FILENAME 			保存当前编辑文件在当前文件夹

v ：进入可视模式（选中）

v motion :w FILENAME		将选中的文本保存在文件夹中

 :r FILENAME			将文件中的文本插入





y motion   			复制

p							粘贴

R                            连续替换

o/O                            下行/上行插入