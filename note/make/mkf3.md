## _*һ��ʵ��*_
```
�ȿ��ļ��ṹ
Dirname
--add.cpp
--add.h
--mult.cpp
--mult.h
calc.cpp
```

## �ٿ�ʹ��make���������
```
calc : 
    gcc add.cpp mult.cpp calc.cpp -o calc.exe
```
#### ��Ȼ���������ǶԵģ����ǻ��������в��㡪���������ã�������������ŵ� : ������Դ�����ٴα����ʱ�򣬻����ı���
```
calc : mult.o add.o
	g++ -c add.o mult.o calc.cpp -o calcNew.exe

add.o : add.cpp
	g++ -c add.cpp -o add.o

mult.o : mult.cpp
	g++ -c mult.cpp -o mult.o
```
## _*�������̲��(<u>g++ main.cpp (-o main.exe)</u>����<u>g++ -lstdc++ main.cpp (-o main.exe)</u>)*_
>>Ԥ���� : gcc -E main.cpp >main.ii(Ԥ�����ļ�)
> 
>>���� : gcc -S main.ii(����ļ�)
> 
>>��� : gcc -c main.s(�������ļ�)
> 
>>���� : g++ -lstdc++ main.o(���ɿ�ִ���ļ�����д��c++�������õ�g++��c������gcc)