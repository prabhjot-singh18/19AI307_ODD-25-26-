##2(E) - ACCESS MODIFIERS
### QUESTION:
Create a class **Calculator** with:
- A **non-static method** `add(int a, int b)` that returns the sum  
- A **static method** `info()` that prints `"Calculator is ready"`

Example:

Input:
```
10
20
```

Output:
```
Calculator is ready
Sum: 30
```

---

### AIM:
To write a Java program that demonstrates the use of static and non-static methods inside a class.

---

### ALGORITHM:

1. Create a class `Calculator` with a non-static method `add()` that returns the sum of two integers.  
2. Define a static method `info()` to print a message indicating readiness.  
3. In the main method, read two integers from the user.  
4. Call the static method directly using the class name or object.  
5. Create an object of Calculator, call the add method, and print the result.

---

### PROGRAM:

```
Program to demonstrate static and non-static methods in a Calculator class
Developed by: PRABHJOT SINGH
RegisterNumber: 212222040116
```

---

### Sourcecode.java:

```java
import java.util.Scanner;

class Calculator {
    public int add(int a, int b){
        return a + b;
    }
    public static void info(){
        System.out.println("Calculator is ready");
    }
}

class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        int a = sc.nextInt();
        int b = sc.nextInt();
        
        Calculator cal = new Calculator();
        cal.info();
        
        int sum = cal.add(a, b);
        System.out.println("Sum: " + sum);
    }
}
```

---

### OUTPUT:
<img width="783" height="312" alt="image" src="https://github.com/user-attachments/assets/8938b3ea-d60b-40a2-9366-f12125f71f5a" />


---

### RESULT:
Thus, the Java program demonstrating static and non-static methods in a class was successfully executed.




