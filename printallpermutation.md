Print All Permutations of a String in CPP
Given a string str, the task is to print all of str permutations. A permutation is an arrangement of all or part of a set of objects in the order in which they are arranged. For example, the words ‘bat’ and ‘tab’ are two different permutations (or arrangements) of a similar three-letter word.
Example :

Input : ABC
Output : ABC ACB BCA BAC CAB CBA

```cpp
public
class Main {
    static void printPermutn(String str, String ans) {
        if (str.length() == 0) {
            System.out.print(ans + " ");
            return;
        }
        for (int i = 0; i < str.length(); i++) {
            char ch = str.charAt(i);
            String r = str.substring(0, i) + str.substring(i + 1);
            printPermutn(r, ans + ch);
        }
    }
    public
    static void main(String[] args) {
        String s = "abb";
        printPermutn(s, "");
    }
}
```

## JAVA

```java
import java.util.Stack;
public class Main {
    static void printPermutn(String str, String ans,Stack newStack) {

        if (str.length() == 0) {
            newStack.push(ans);
            return;
        }
        for (int i = 0; i < str.length(); i++) {

            char ch = str.charAt(i);

            String r = str.substring(0, i) + str.substring(i + 1);

            printPermutn(r, ans + ch,newStack);
        }
    }

    public static void main(String[] args) {
        Stack<String> newStack = new Stack<String>();
        String s = "abc";
        printPermutn(s, "",newStack);
        // newStack.peek();
        while(!newStack.empty()){
            System.out.println(newStack.pop());
        }
    }
}
```
