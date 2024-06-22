Length of the String using Recursion in C++
Here, the program to find the length of the string using recursion in C++ programming language. We are given with a string and need to print its length. Besides the recursive approach to solve this problem we will also discuss the iterative and using inbuilt function to find the length of the given input string.
Example :
Input : String : PrepInsta
Output : 9

```cpp
#include <bits/stdc++.h>
using namespace std;

int Len(char* str) 
{
   if (*str == '\0')
      return 0;
   else
      return 1 + Len(str + 1);
}

/* Driver code */
int main()
{
   char str[] = "Akshay";
   cout << Len(str);
   return 0;
}
```

## Java
```java
public class Main
{
     //Function to calculate length
    private static int recLength(String str)
    {
        // if we reach at the end of the string
        if (str.equals(""))
            return 0;
        else
            return recLength(str.substring(1)) + 1;
    }

    //Driver program to test the function 
    public static void main(String[] args)
    {
        String str ="Akshay";
        System.out.println("length of the string "+recLength(str));
    }
}
```
