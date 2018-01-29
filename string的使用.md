# string的使用

```c++
#include <string>
string s;//此时s是空串
s.size() == s.length();
s.begin()	 s.end()
查找
string s == LONG_LONG_MAX*2 + 1；
s.find('c') == string::npos//没找到
s.find('c') ！= string::npos//找到了
'c'可换成"kjdsd";
strstr(str1,str2) 函数用于判断字符串str2是否是str1的子串。如果是，则该函数返回str2在str1中首次出现的地址；否则，返回NULL。
倒置
reverse(s.begin(),s.end())//同样适用于vector
添加
s = s + 'c';
s = s + "123";
s = "123" + s;
s  'c' +  s;
s.append(s1,pos,n)//从下标pos ,取n个字符加到s尾部
取子串
s1 = s.substr(pos,n)//从下标pos ,取n个字符拼串 赋值给s1；

```

