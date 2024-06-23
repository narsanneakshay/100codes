# ALGORITHMS
## SORTING
### BUBBLE SORT : 

![image](https://github.com/narsanneakshay/100codes/assets/173332971/778ba44d-3940-4d50-8adb-a5de19c7bee3)


```cpp
#include <iostream>
using namespace std;

template <typename T>
void swap_values(T &a, T &b) {
    T temp = a;
    a = b;
    b = temp;
}

void bubble_sort(int *array,int size){
    for(int i=0;i<size;i++){
        for(int j=0;j<size-i-1;j++){
            if(array[j]>array[j+1]){
                swap_values(array[j],array[j+1]);
            }
        }
    }
}
int main()
{
    int n;
    cout<<"Enter the size of array : ";
    cin>>n;
    int array[n];
    cout<<"Enter the elements of array : "<<endl;
    for(int i=0;i<n;i++){
        cin>>array[i];
    }
    bubble_sort(array,n);
    for(int i=0;i<n;i++){
        cout<<array[i]<<" ";
    }
    return 0;
}
```

```java
import java.util.Scanner;

public class BubbleSort {

    public static <T> void swap_values(T[] array, int i, int j) {
        T temp = array[i];
        array[i] = array[j];
        array[j] = temp;
    }

    public static void bubble_sort(int[] array, int size) {
        for (int i = 0; i < size; i++) {
            for (int j = 0; j < size - i - 1; j++) {
                if (array[j] > array[j + 1]) {
                    int temp = array[j];
                    array[j] = array[j + 1];
                    array[j + 1] = temp;
                }
            }
        }
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter the size of array: ");
        int n = scanner.nextInt();

        int[] array = new int[n];

        System.out.println("Enter the elements of array: ");
        for (int i = 0; i < n; i++) {
            array[i] = scanner.nextInt();
        }

        bubble_sort(array, n);

        System.out.println("Sorted array: ");
        for (int i = 0; i < n; i++) {
            System.out.print(array[i] + " ");
        }
    }
}
```

### INSERSION SORT :


![image](https://github.com/narsanneakshay/100codes/assets/173332971/61e6c90c-e839-411a-9683-b7b57792e173)


```cpp
#include <iostream>
using namespace std;

template <typename T>
void swap_values(T &a, T &b) {
    T temp = a;
    a = b;
    b = temp;
}

void insersion_sort(int *array,int size){
    for(int i=1;i<size;i++){
        int j=i-1;
        int key = array[i];
        while(j>=0 && array[j]>key){
            array[j+1] = array[j];
            j=j-1;
        }
        array[j+1] = key;
    }
}
int main()
{
    int n;
    cout<<"Enter the size of array : ";
    cin>>n;
    int array[n];
    cout<<"Enter the elements of array : "<<endl;
    for(int i=0;i<n;i++){
        cin>>array[i];
    }
    insersion_sort(array,n);
    for(int i=0;i<n;i++){
        cout<<array[i]<<" ";
    }
    return 0;
}
```

```java
import java.util.Scanner;

public class Main {

    public static <T> void swap_values(T[] array, int i, int j) {
        T temp = array[i];
        array[i] = array[j];
        array[j] = temp;
    }

    public static void bubble_sort(int[] array, int size) {
        for (int i = 1; i < size; i++) {
            int key = array[i];
            int j=i-1;
            while(j>=0 && array[j]>key){
                array[j+1] = array[j];
                j = j-1;
            }
            array[j+1] = key;
        }
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter the size of array: ");
        int n = scanner.nextInt();

        int[] array = new int[n];

        System.out.println("Enter the elements of array: ");
        for (int i = 0; i < n; i++) {
            array[i] = scanner.nextInt();
        }

        bubble_sort(array, n);

        System.out.println("Sorted array: ");
        for (int i = 0; i < n; i++) {
            System.out.print(array[i] + " ");
        }
    }
}

```
