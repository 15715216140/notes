# sort的使用

```c++
sort(a,a+5)//排序a首元素到a+4地址所在元素；
  sort 	快排和插排

stable_sort	 归并

partail_sort	 堆排

sort默认从小到大，也可自行定义com



stable_sort 与sort用法相同

sort(a,a+5,)

sort(a,a+5,less<int>())

sort(a,a+5,greater<int>())

com函数

bool com(){

}
sort(a,a+5,cmp);

部分排序
partial_sort(a,a+2,a+5)
partial_sort(v.begin(),v.begin+5,v.end(),com)//部分排序前5个
nth_element(v.begin(),v.begin()+6,v.end())//第七名，v.begin()+6的地址所在元素；
  
结构体排序  
  struct stu{
    int a;
    int b;
  }a[5];
bool comp(stu x,stu y){
  if(a == b)  { return x.b < y.b;}
  else	return x.a < y.a ;
}
sort(a,a+5,comp);



```







