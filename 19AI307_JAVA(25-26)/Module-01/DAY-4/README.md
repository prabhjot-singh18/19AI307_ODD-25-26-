## Ex.No:1(D) ARRAYS


### QUESTION:
Write a Java program that reads an array of integers and a value, then prints all the elements in the array that are greater than the given value.

Example:

Input:  
```
5  
10  
20  
30  
40  
50  
25
```
Output:  
```
30  
40  
50
```

---

### AIM:
To write a Java program that reads an array of integers and prints only those elements which are greater than a specified value.

---

### ALGORITHM:

1. Read the size of the array from the user.  
2. Input all elements into the array.  
3. Read the comparison value.  
4. Traverse the array and check if each element is greater than the given value.  
5. Print all elements that satisfy the condition or print a message if none are found.

---

### PROGRAM:

```
Program to print all array elements greater than a given value
Developed by: PRABHJOT SINGH
RegisterNumber: 212222040116
```

---

### Sourcecode.java:

```java
import java.util.*;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        
        int n = sc.nextInt();
        int[] arr = new int[n];
        
        for(int i = 0; i < n; i++){
            arr[i] = sc.nextInt();
        }
        
        int count = 0;
        int val = sc.nextInt();
        
        for(int i = 0; i < n; i++){
            if(arr[i] > val){
                System.out.println(arr[i]);
                count++;
            }
        }
        
        if(count == 0) 
            System.out.print("No elements greater than " + val);
    }
}
```

---

### OUTPUT:
<img width="674" height="234" alt="image" src="https://github.com/user-attachments/assets/6da56e1b-b099-4c76-8fc3-074b0c1e2d79" />


---

### RESULT:
Thus, the Java program to print array elements greater than a given value was successfully executed.




