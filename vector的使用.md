

# 容器的使用



```c++
#include <vecoter>
{ 
  初始化
  //vector从0下标开始；
  vector<int> v， v1;//空容器
  vector<int> v(3)//包含3个元素；
  vector<int> v(3,9)//包含3个元素,每个元素都是9；
  vector<int> v(v1)//copy v1;
  int a[3] = {0,1,2};
  vector<int> v(a,a+3)//copy a数组；
  
  状态
  v.size()//返回v个数，空是时候是0，空时不可atuo i = v.begin();
  v.begin()//首地址
  v.end()//末元素地址+1；for里终止条件 auto i != v.end(); i < end(); i <= v.end()-1;
    	 //有点像数组最后一位的空位置
  v.at(i) == v[i]//推荐使用后者；
  bool is = v.empty();/空返回true，不空返回false;
  v.push_back(n)//在尾部添加n进容器；
  v.pop_back()//删除尾元素；
  二维容器
  vector<vector<int>> v1;
  vector<int> v[5];
  vector<>
    
  vector<vector<int>> ans(r,vector<int>(c));//初始化r行c列的容器
  v1.size()//v1有几行
  v1[i].size()//v1[i]几行有几个元素，即有几列

    
  遍历
  for(int i : v)
    	cout << i;
  for(auto i = v.begin() ; i < v.end() ; i++ ) 
		cout << *i;////auto 推荐使用；
   for(auto i = v.begin() ; i ！= v.end() ; i++ ) 
		cout << *i;
  for(vector<int>::iterator it = vecIntB.begin() ;it!=vecIntB.end();it++)   
        cout<<*it;
 
    
  删除
    v.erase(v.begin()+2)//删除第3个元素（v.begin()+2地址所在）；
    v.erase(v.begin()+2，v.begin()+5)//删除第3-5个元素
    v.erase(v.begin(),v.end());//清空
    v.clear() ;//清空；
    v.begin()+1//允许这样操作  
  v.pop_back() & v.erase() & v.push_back 后 v.size() 会变；
    
       
    如有错误，欢迎指正，如有不足，欢迎补充。
} 
```

欢迎造访我的[www.github.com/15715216140](www.github.com/15715216140)