#伪目标，防止有文件与命令重命
.PHONY:com_1
.PHONY:com_2
.PHONY:com_3
.PHONY:com_4
.PHONY:com_5
.PHONY:com_6
.PHONY:com_7
.PHONY:com_8
.PHONY:com_9

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

#wildcard函数用于展开指定文件
var9=$(wildcard ./*.c ./test/*.c)
com_5:
	@echo $(var9)

#notdir函数用于去掉路径，只留文件名
var10:=$(wildcard ./*.c ./test/*.c)
var10:=$(notdir $(var10))
com_6:
	@echo $(var10)

#dir函数用于取出路径，即去掉文件名
var11:=$(wildcard ./*.c ./test/*.c)
var11:=$(dir $(var11))
com_7:
	@echo $(var11)

#patsubst函数用于替换文件后缀
var12:=$(wildcard ./*.c ./test/*.c)
var12:=$(notdir $(var12))
var13:=$(patsubst %.c,%.o,$(var12))
#等同于$var13:=(var12:%.c=%.o)
com_8:
	@echo $(var13)

#foreach格式：$(foreach <var>,<list>,<text>)，用于将参数<list>中的单词注意取出
#放到指定的<var>变量中，然后执行<text>所包含的表达式，每一次<text>会返回一个字
#符串
var14:=$(wildcard ./*.c ./test/*.c)
var14:=$(dir $(var14))
var15:=$(foreach n,$(var14),$(wildcard $(n)*.c))
com_9:
	@echo $(var15)

