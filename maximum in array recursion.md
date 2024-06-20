Largest Element of  the array using Recursion in C++
Here, we will discuss the program to find the largest element of the array using recursion in C++ programming language. We are given with an array and we need to print the largest element among the elements of the array.

Example :

Input : arr[6] = {13, 89, 76, 43, 7, 90}
Output : Largest Element is 90
```cpp
#include <iostream>
using namespace std;

int maximum(int *arr,int size,int i=0){
    if(i>=size-1) return arr[i];
    return max(arr[i],maximum(arr,size,i+1));
}

int main()
{
    int n;
    cout<<"Enter size of array"<<endl;
    cin>>n;
    int arr[n];
    for(int i=0;i<n;i++){
        cin>>arr[i];
    }
    cout<<"maximum element in array is : "maximum(arr,n)<<endl;
    return 0;
}
```
