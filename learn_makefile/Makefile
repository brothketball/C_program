#伪目标，防止有文件与命令重命
.PHONY:com_1
.PHONY:com_2
.PHONY:com_3
.PHONY:com_4

#:= 相当于C语言当中的=
var1:=aaa
var2:=$(var1)bbb
var1:=ccc
com_1:
	echo $(var2)

#= 延迟赋值，变量存储最后的赋值
var3=aaa
var4=$(var3)bbb
var3=ccc
com_2:
	echo $(var4)

#?= 若变量前面未赋值，则赋值；若变量已赋值，则不赋值
var5:=aaa
var5?=ccc
var6:=$(var5)bbb
com_3:
	echo $(var6)

#+= 追加赋值，追加赋值与原赋值之间多一个空格，与加\同时换行再追加的效果相同
#或者直接加空格
var7:=aaa
var7+=ccc
var8:=$(var7)bbb
com_4:
	@echo $(var8)
	#echo前加上@，可以使echo命令行不显示

#自动化变量练习在add_makefile中
