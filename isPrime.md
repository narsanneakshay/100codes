Prime Number Using Recursion in C++
Here, in this page we will discuss the program to check a number is prime number using recursion in C++ programming language. We are given with a number and check if it is prime or not. We will discuss both recursive and non-recursive approach to check if a given number is prime or not. A number is prime, if it is divisible by 1 and number itself.

Example :

Input : Number : 34
Output : No
Explanation : 34 is not a prime number, as factors of 34 are 1, 2, 17, 34.
```cpp
#include <iostream>
using namespace std;

bool isPrime(int n,int i = 2){
    if(n==i) return true;
    if(n%i==0)return false;
    return isPrime(n,i+1);
}

int main()
{
    int n;
    cout<<"Enter number"<<endl;
    cin>>n;
    if(isPrime(n)){
        cout<<n<<" : is prime number"<<endl;
    }else{
        cout<<n<<" : is not a prime number"<<endl;
    }
    return 0;
}
```
