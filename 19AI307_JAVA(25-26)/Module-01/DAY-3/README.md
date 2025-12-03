## Ex.No:1(C) LOOPING STATEMENT

### QUESTION:
Write a Java program to print all prime numbers within a given range.  
The user provides two integers: the start and end of the range.  
The program must display all prime numbers between these two values (inclusive).

Example:  
Input: `10 20`  
Output: `Prime numbers: 11 13 17 19`

---

### AIM:
To write a Java program that takes a range of integers as input and prints all the prime numbers within the given range.

---

### ALGORITHM:

1. Read the starting number and ending number of the range from the user.  
2. Iterate through every number between the start and end values.  
3. For each number, check whether it is prime using a helper function.  
4. If the number is prime, print it.  
5. Continue until the entire range has been processed.

---

### PROGRAM:

```
Program to print all prime numbers in a given range
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
        int start = sc.nextInt();
        int end = sc.nextInt();
        System.out.print("Prime numbers:");
        for(int i = start; i <= end; i++){
            if(isPrime(i)){
                System.out.print(" " + i);
            }
        }
    }
    
    static boolean isPrime(int n){
        if(n <= 1) return false;
        if(n == 2) return true;
        if(n % 2 == 0) return false;
        for(int i = 3; i * i <= n; i += 2){
            if(n % i == 0) return false;
        }
        return true;
    }
}
```

---

### OUTPUT:
<img width="692" height="248" alt="image" src="https://github.com/user-attachments/assets/b75fb586-9de8-47f5-8a64-de32ea4807ae" />


---

### RESULT:
Thus, the Java program to print all prime numbers within a given range was successfully executed.



