LCM of Two Numbers using Recursion in C++
Here, the program to find the LCM of Two numbers using Recursion in C++ Programming Language. We are given with two integers and need to find the LCM of the given numbers.  The LCM of two integers num1 and num2 is the smallest positive integer that is perfectly divisible by both num1 and num2(without a remainder). 

Example :

Input : num1 = 3 num2 = 21
Output : LCM of 3 and 21 is 21.

## CPP
```cpp
#include<bits/stdc++.h>
using namespace std;

int getHCF(int num1, int num2)
{
   if (num1 == 0)
      return num2;

   if (num2 == 0)
      return num1;

   if (num1 == num2)
      return num1;

   if (num1 > num2)
      return getHCF(num1 - num2, num2);

   return getHCF(num1, num2 - num1);
}

int main()
{
   int num1 =0;
   int num2 = 0;
   cout<<"Enter number 1 and number 2"<<endl;
   cin>>num1>>num2;

   int HCF = getHCF(num1, num2);
    int LCM = (num1*num2)/HCF;
   cout<<"HCF of "<<num1<<" and "<<num2<<" is "<<HCF<<endl;
   cout<<"HCF of "<<num1<<" and "<<num2<<" is "<<LCM<<endl;

   return 0;
}
```

## JAVA
```java
import java.util.Scanner;
public class Main
{
	public static void main(String[] args) {
	    Scanner sc = new Scanner(System.in);
	    System.out.println("Enter number 1");
	    int number1 = sc.nextInt();
	    System.out.println("Enter number 2");
	    int number2 = sc.nextInt();
	    int HCF = calculateHCF(number1,number2);
	    System.out.println("Hcf of two numbers is : "+HCF);
	    int LCM = (number1*number2)/HCF;
	    System.out.println("LCM of two numbers is : "+LCM);
	    
	    
	}
	public static int calculateHCF(int num1,int num2){
	    if(num1 == 0) return 0;
	    if(num2 == 0) return 0;
	    if(num1 == num2) return num1;
	    if(num1>num2) return calculateHCF((num1-num2),num2);
	    return calculateHCF(num1,(num2-num1));
	}
}
```
