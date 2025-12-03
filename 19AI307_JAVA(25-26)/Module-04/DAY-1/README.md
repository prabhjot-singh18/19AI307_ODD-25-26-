# Ex.No:4(A) EXCEPTION HANDLING
## Ex.No:15 HANDLING NULL VALUES IN STRING ARRAY

### QUESTION:
You wrote a program that stores some input strings into a String array and prints each string in uppercase.  
However, you're getting a NullPointerException.  
What should you check in your array before calling `.toUpperCase()` on an element?

---

### AIM:
To write a Java program that safely handles null string values before converting them to uppercase.

---

### ALGORITHM:

1. Read a string from the user.  
2. Check if the string is null.  
3. If it is null, print a message.  
4. Otherwise, convert it to uppercase.  
5. End the program.

---

### PROGRAM:

```
Program to handle null values before calling toUpperCase()
Developed by: PRABHJOT SINGH
RegisterNumber: 212222040116
```

---

### Sourcecode.java:

```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String input = sc.nextLine();
        
        if (input == null || input.equals("null"))
            System.out.println("Null element");
        else
            System.out.println(input.toUpperCase());
    }
}
```

---

### OUTPUT:
<img width="701" height="243" alt="image" src="https://github.com/user-attachments/assets/cf64c571-40c7-4648-a94c-429e1ee74cf5" />


---

### RESULT:
Thus, the Java program to safely check for null values before calling `toUpperCase()` was successfully executed.



