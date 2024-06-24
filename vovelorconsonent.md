```java
import java.util.Scanner;
public class Main
{
	public static void main(String[] args) {
	    Scanner sc = new Scanner(System.in);
	    String ch = sc.next();
	    checkChar(ch);
	}
	private static void checkChar(String string){
	    char ch = string.charAt(0);
	    if(ch == 'A' || ch == 'E' || ch == 'I' || 
	    ch == 'O' || ch=='U' ||ch == 'a' || ch == 'e'
	    || ch == 'i' || ch == 'o' || ch=='u'){
	        System.out.println("It is Vovel");
	    }else{
	        System.out.println("It is consonent");
	    }
	}
}
```
