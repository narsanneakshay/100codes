Reversing a Number using Recursion in C++
Here, in this page we will discuss the program for reversing a number using recursion in C++ programming language. We are given with a number and need to print the reverse of the given number. We will discuss the both recursive and non-recursive method to find the reverse of the given input number.

Example :

Input : 1234
Output : 4321

## CPP
```cpp
#include <iostream>
using namespace std;

int reverseNumber(int n, int reversed);

int main() {
    int n;
    cout << "Enter the Number: ";
    cin >> n;
    cout << "Reverse number is: " << reverseNumber(n, 0) << endl;
    return 0;
}

int reverseNumber(int n, int reversed) {
    if (n == 0) {
        return reversed;
    }
    int digit = n % 10;
    reversed = reversed * 10 + digit;
    return reverseNumber(n / 10, reversed);
}
```

## Java

```java
import java.util.Scanner;
public class Main
{
	public static void main(String[] args) {
            Scanner sc = new Scanner(System.in);
            System.out.println("Enter the Number");
            int n = sc.nextInt();
            System.out.println("reverse number is : " + reverseNumber(n,0)+ "");
	}
	private static int reverseNumber(int n, int reversed) {
        if (n == 0) {
            return reversed;
        }
        int digit = n % 10;
        reversed = reversed * 10 + digit;
        return reverseNumber(n / 10, reversed);
    }
}
```
