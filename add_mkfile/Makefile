#变量赋值
var:=main.o input.o calcu.o

main:$(var)
	gcc -o main $^
	#$^代表所有依赖，这里即$(var)

%.o:%.c
	#通配符%，相当于Linux中的*
	gcc -c $< -o $@
	#$<代表目标文件，这里即%.o；&@代表依赖，这里即%.c

.PHONY:clean
clean:
	rm *.o
	rm main
