# map的使用

```c++
map和set一样，自动排序，从小到大
初始化
map<int,char> m;
操作
m.begin(); m.end();
m.begin()->first; m.begin()->second;


查找

if(m.find(2) != m.end())//找到此元素，返回该元地址，否则返回m.end();
m.count(5); //返回5作为关键字的个数，只能返回0或1；
		   //用此代替find()查找更好用；
if(m[2] == 0);//不建议这样，这样m[2]也会被收进m里；

m.size();//返回个数；
```

# pair

```c++
当一个函数需要返回两个值时，使用pair更方便
pair<int,int> m;
m.first = 1;
m.second = 2;
```

