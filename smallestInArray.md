Smallest Element of  the array using Recursion in C++
 
Here, program to find smallest element of the array using recursion in C++. We are given with an array and we need to print the smallest element. We will discuss the approach using recursion and iteratively both to find the smallest element.

Example :

Input : arr[6]= {10, 7, 78, 67, 89, 12}
Output :  Smallest Element is : 7

## C++ Code
```cpp
#include <bits/stdc++.h>
using namespace std;

int minimum(int *array,int size){
    int mini = INT_MAX;
    for(int i=0;i<size;i++){
        if(mini>array[i]){
            mini = array[i];
        }
    }
    return mini;
}

int main()
{
    int n;
    cout<<"Enter the size of array"<<endl;
    cin>>n;
    int array[n];
    for(int i=0;i<n;i++){
        cin>>array[i];
    }
    cout<<"Minimum in the array is :"<<minimum(array,n)<<endl;
    return 0;
}
```
## Java Code
```java
import java.util.Scanner;
public class Main
{
	public static void main(String[] args) {
	    Scanner sc = new Scanner(System.in);
	    System.out.println("Enter the size of array");
        int n = sc.nextInt();
        int []Array  = new int[n];
        for(int i=0;i<n;i++){
            Array[i] = sc.nextInt();
        }
        System.out.println("Minimum element in the array is : "+minimun(Array,n));
	}
	public static int minimun(int []array , int size){
	    int maximum_ele = Integer.MAX_VALUE;
	    for(int i=0;i<size;i++){
	        if(maximum_ele>array[i]){
	            maximum_ele = array[i];
	        }
	    }
	    return maximum_ele;
	}


}
```
