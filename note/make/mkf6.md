# _*1 . make编译动态链接库*_
<img src="src/fordll.png" alt="">
<img src="src/link.png" alt="">

## 命令
g++ -shared -fPIC name.cpp -o name.dll

## 使用
g++ main.cpp name.dll -o main.exe

##  好处
使用动态链接库的程序，你可以在修改动态链接库对应源代码时，只需要重新编译该代码就行，这样会更省时

# _*2 . 静态链接库*_
<img src="src/sta.png" alt="">  
  

## 命令  
  
#### g++ -c alib.cpp -o alib.o  

#### ar -r alib.lib alib.o