## Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

### QUESTION:
Lovely enters a mystical Power Chamber with 10 doors. Behind each door is a magic symbol that changes her power using compound assignment operators.  
She starts with an initial power value and the following operations occur at each door:

1. `+= 5`  
2. `-= 3`  
3. `*= 2`  
4. `/= 4`  
5. `%= 3`  
6. `&= 7`  
7. `^= 4`  
8. `<<= 1`  
9. `>>= 1`  

Input: One integer (initial power)  
Output: Display the power after every door and the final power.

---

### AIM:
To write a Java program that updates an initial power value using various compound assignment operators and displays the result after each operation.

---

### ALGORITHM:

1. Start the program and read the initial power value from the user.  
2. Print the initial power before applying any operations.  
3. Apply each compound assignment operator in the given sequence.  
4. After every operation, print the updated power.  
5. After all 10 operations, print the final power.

---

### PROGRAM:

```
Program to implement variables and Operators using Java
Developed by: PAVAN KUMAR A B
RegisterNumber: 212222040113
```

---

### Sourcecode.java:

```java
import java.util.*;
public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        
        int n = sc.nextInt();
        System.out.println("Initial Power = " + n);
        System.out.println("After Door 1 (+= 5): " + (n += 5));
        System.out.println("After Door 2 (-= 3): " + (n -= 3));
        System.out.println("After Door 3 (*= 2): " + (n *= 2));
        System.out.println("After Door 4 (/= 4): " + (n /= 4));
        System.out.println("After Door 5 (%= 3): " + (n %= 3));
        System.out.println("After Door 6 (|= 2): " + (n |= 2));
        System.out.println("After Door 7 (&= 7): " + (n &= 7));
        System.out.println("After Door 8 (^= 4): " + (n ^= 4));
        System.out.println("After Door 9 (<<= 1): " + (n <<= 1));
        System.out.println("After Door 10 (>>= 1): " + (n >>= 1));
        System.out.println("Final Power = " + n);
    }
}
```

---

### OUTPUT:
<img width="525" height="281" alt="image" src="https://github.com/user-attachments/assets/4a92e8bd-e988-4e41-a749-6817ed61d932" />


---

### RESULT:
Thus, the Java program using compound assignment operators to update the power value was successfully executed.

