## Ex.No:2(B) METHODS
### QUESTION:
Write a method `int cube(int x)` that internally calls another method `int square(int x)` to compute the cube using the formula:

```
cube(x) = x * square(x)
```

Example:

Input:
```
5
```
Output:
```
125
```

---

### AIM:
To write a Java program that demonstrates method calling within another method by using a `square()` method inside a `cube()` method.

---

### ALGORITHM:

1. Define a method `square(int x)` that returns the square of the given number.  
2. Define another method `cube(int x)` that calls `square(x)` and multiplies the result by `x`.  
3. In the main method, read an integer input from the user.  
4. Call the `cube()` method and store or print the result.  
5. Display the final computed cube value.

---

### PROGRAM:

```
Program to compute cube of a number using the square() method
Developed by: PRABHJOT SINGH
RegisterNumber: 212222040116
```

---

### Sourcecode.java:

```java
import java.util.*;

public class Main{
    public static int square(int x){
        return x * x;
    }
    
    public static int cube(int x){
        return square(x) * x;
    }
    
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        
        int x = sc.nextInt();
        System.out.print(cube(x));
    }
}
```

---

### OUTPUT:
<img width="538" height="161" alt="image" src="https://github.com/user-attachments/assets/8aad4fa1-c181-415c-b2e6-66e548158b2e" />


---

### RESULT:
Thus, the Java program demonstrating method calling within another method to compute the cube of a number was successfully executed.


