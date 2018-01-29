# bitset c++

http://blog.csdn.net/qll125596718/article/details/6901935

原博主写的更细（推荐去看一看），本人自己整理，增改了一些，便于记忆理解

```c++
#include <bitset>

0101101010//一个bitset类型的变量
9876543210//对应元素的下标

初始化
using std :: bitset

bitset<5> bit1("11101")//最简单的初始化
！！！ bit1 = bit2//没有这个操作，编译不通过

bitset<n> b;            //b有n位，每位都为0  
bitset<n> b(u);             //b是unsigned long型u的一个副本  
bitset<n> b(s);             //b是string对象s中含有的位串的副本  
bitset<n> b(s, pos, n);     //b是string对象s中pos位置开始个n素的拷贝
bitset在定义时，要明确bitset含有多少位，须在尖括号内给出长度值;
如bitset<32> bitvec; //32位，全为0

不满左边补0
string s = "101";//若(string s = "102")会运行奇怪的错误，bitset报错；
bitset<10> bit1(s)//即先把101摆在那，剩余的7位（下标从3-9）在左面用0补；
				//bit1:0000000,101 (请忽略','那是我为了方便理解加的，实际并不存在)

溢出从左截取；
string s = "001111111"
bitset<5> bit1(s)//最终截取字符串前几位：00111；
  				////bit1:00111
  
取部分
string s = "001111"
bitset<10> bit1(s，1)
//最终截下标为1到最后的元素，即先把01111摆在那，剩余的5位（下标从5-9）在左面用0补
//bit1：00000,01111 (请忽略','那是我为了方便理解加的，实际并不存在)
  
bitset<10> bit1(s，1，2）//从下标为1，截取2个元素，即先把01摆在那，剩余的8位（下标从2-9）在左面用0补
//bit1：00000000，01   (请忽略','那是我为了方便理解加的，实际并不存在)        

查找
bitset<10> bit1;
bit1.size()//返回二进制总位数；
bit1.count()//返回bit1里1的个数；
bool is = bit1.any()//  is = if(bit1.count() >= 1)    
bool is = bit1.none()// is = if(bit1.count() == 0)
bool is = bit[5].test// is = bit1.[5]; 即测试 bit1[5]==1？
                
操作 
bit1.set()//所有位设为1
bit1.set(pos)//下标为pos的位设为1
bit1.reset//所有位设为0
bit1.reset(pos)//下标为pos的位设为0
bit1.flip()//所有位取反
bit1.flip(pos)//pos位取反
bit1.to_ulong()//返回一个usign long long 整数


                
                
                		
                     


```

