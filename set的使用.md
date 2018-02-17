# set使用技巧

```c++
#include <set>
{
  set中会自动排序，由小到大，插入时，红黑树
  set<int> s;// char string 
  
  int arr[5] = {0,1,2,3,4};
  set<int> iset(arr,arr+5);
  vector<int>::iteartor it;
  
  s.begin() //s首地址
  *s.begin()//首元素；    
   s.begin()++//允许
   s.begin+1//不允许
  
  s.size()//元素个数；
  s.insert(n);//插入n;
  s.clear()//清空s;
  bool is = s.empty();
  循环
    for(int i : s) 
      cout << i;
  	for(auto i  = s.begin(); i <= s.end(); i++)
      cout << *i;
  查找
  s.find(n) == s.end()//没找到，一直查到尾
  s.find(n) != s.end()//找到了，停在找到的位置了
  s.count(n) == 1//有次元素，找到了
  s.count(n) == 0//无此元素，没找到
  it = s.find(n)//
  擦除
   s.erase(n)//删除n;
   s.earse(s.begin(),it)//删除到it前一个地址
   
  
}
```

