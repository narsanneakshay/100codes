Power of a Number using Recursion in C++
 

Here, in this page we will discuss the program to find power of a number using recursion in C++ programming language. We are given with two integers values base and power respectively. We need to print the value representing the base raise to its power. We will design the program using recursion and also discuss the approach using iteration as well.

Example :

Input : 5 3
Output : 125
Explanation : 53 = 125
```cpp
#include <iostream>
using namespace std;

long long calculatePower(int n,int x){
    if(x==0)return 1;
    return n*calculatePower(n,x-1);
}

int main()
{
    int n;
    cout<<"Enter number"<<endl;
    cin>>n;
    int x;
    cout<<"Enter power to calculate"<<endl;
    cin>>x;
    cout<<calculatePower(n,x)<<endl;
    return 0;
}
```
![alt text](image.png)