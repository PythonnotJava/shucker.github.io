## _*1 . makefile�е�αĿ��(.PHONY:clean)*_

>> ������αĿ��֮��makefile�������ж�Ŀ���Ƿ���ڻ���Ŀ���Ƿ���Ҫ����;
>> ����Makefile�ж����ִ�������Ŀ���ʵ���ļ�����ͻ
>>

## _*2 . ģʽƥ�䡪��%Ŀ��:%����*_

#### %��Ŀ�����������ͬ���ֵ�ͨ��

<img src="src/mod.png" alt="">

## _*3 . һ��ģʽƥ��İ���*_

```
%.o : %.cpp
	$(CXX) -c $^ -o $@
```

��������ģʽƥ����Դ����������ķ�����ǰ�������������˲��ҵĹ���

```
add.o : add.cpp
	$(CXX) -c $^ -o $@


main.o : main.cpp
	$(CXX) -c $^ -o $@
```

```
# ���������������Ĺ���
OBJ = add.o main.o(����дOBJ =  $(patsubst %.cpp, %.o, $(wildcard ./*.cpp)))
TARGET = main
```

#### �滻����

```
SRC := main.c add.cpp
OBJF := $(SRC:.cpp=.o)
all:
	@echo "SRC = $(SRC)"
	@echo "OBJF = $(OBJF)"
```
