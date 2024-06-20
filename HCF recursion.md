HCF of Two Numbers using Recursion in C++
Here, the program to find the HCF of Two numbers using recursion in C++. We are given with two numbers and need to find the HCF of the given two numbers.The HCF or the Highest Common Factor of two numbers is the largest common factor of two or more values.

Example :

Input : a = 96, b = 56
Output : HCF of 96 and 56 is 8.

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

   cout<<"HCF of "<<num1<<" and "<<num2<<" is "<<HCF;

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
	    System.out.println("Hcf of two numbers is : "+calculateHCF(number1,number2));
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
