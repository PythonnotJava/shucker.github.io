# _*1 . make���붯̬���ӿ�*_
<img src="src/fordll.png" alt="">
<img src="src/link.png" alt="">

## ����
g++ -shared -fPIC name.cpp -o name.dll

## ʹ��
g++ main.cpp name.dll -o main.exe

##  �ô�
ʹ�ö�̬���ӿ�ĳ�����������޸Ķ�̬���ӿ��ӦԴ����ʱ��ֻ��Ҫ���±���ô�����У��������ʡʱ

# _*2 . ��̬���ӿ�*_
<img src="src/sta.png" alt="">  
  

## ����  
  
#### g++ -c alib.cpp -o alib.o  

#### ar -r alib.lib alib.o