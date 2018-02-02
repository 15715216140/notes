binary_search() & upper_bound() & lower_bound()



```c++
vector<int> a = {0,1,2,2,3,4};
使用前提是a已经升序排好了
cout << binary_search(a.begin(),a.end(),2);//a,a+3迭代位置（a->a+2地址所在），查找2
							//return ture or false
upper_bound(a.begin(),a.end(),2)//返回指针
			 	 			 //从左往右，返回第一个比  大于  的该数的地址，
			 				 //找不到就返回最后一个元素的下一位 a.end()
lower_bound(a.begin(),a.end(),2)//返回指针
			 	 			 //从左往右，找到第一个  大于等于  该数的地址，
			 				 //找不到就返回最后一个元素的下一位 a.end()
当cout << binary_search(a.begin(),a.end(),2) == false;
则lower_bound(a.begin(),a.end(),2) == upper_bound(a.begin(),a.end(),2)
```

