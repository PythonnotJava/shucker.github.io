## _*一个实例*_
```
先看文件结构
Dirname
--add.cpp
--add.h
--mult.cpp
--mult.h
calc.cpp
```

## 再看使用make编译的命令
```
calc : 
    gcc add.cpp mult.cpp calc.cpp -o calc.exe
```
#### 虽然这样编译是对的，但是还是有美中不足——这样不好，下面命令更有优点 : 当更换源代码再次编译的时候，会更快的编译
```
calc : mult.o add.o
	g++ -c add.o mult.o calc.cpp -o calcNew.exe

add.o : add.cpp
	g++ -c add.cpp -o add.o

mult.o : mult.cpp
	g++ -c mult.cpp -o mult.o
```
## _*编译流程拆分(<u>g++ main.cpp (-o main.exe)</u>或者<u>g++ -lstdc++ main.cpp (-o main.exe)</u>)*_
>>预处理 : gcc -E main.cpp >main.ii(预处理文件)
> 
>>编译 : gcc -S main.ii(汇编文件)
> 
>>汇编 : gcc -c main.s(二进制文件)
> 
>>链接 : g++ -lstdc++ main.o(生成可执行文件，我写的c++，所以用的g++，c语言用gcc)