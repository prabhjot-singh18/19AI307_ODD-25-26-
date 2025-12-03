# Ex.No:5(A) INPUTSTREAMREADER 
### QUESTION:
Write a Java program to create a log file where every user input is stored along with a timestamp.  
Logging stops when the user types **exit**.

Example:

Input:
```
welcome
hi
exit
```

Output:
```
Logging stopped. Check user_log.txt
```

---

### AIM:
To write a Java program that logs user input with timestamps into a text file until the user enters "exit".

---

### ALGORITHM:

1. Create or open a log file named `user_log.txt` in append mode.  
2. Continuously read input from the user.  
3. For each line, write a timestamp followed by the user input into the log file.  
4. Stop when the user enters `"exit"`.  
5. Close resources and display a confirmation message.

---

### PROGRAM:

```
Program to log user input with timestamps into a file
Developed by: PRABHJOT SINGH
RegisterNumber: 212222040116
```

---

### Sourcecode.java:

```java
import java.io.BufferedWriter;
import java.io.FileWriter;
import java.io.IOException;
import java.time.LocalDateTime;
import java.time.format.DateTimeFormatter;
import java.util.Scanner;

public class UserInputLogger {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String fileName = "user_log.txt";
        DateTimeFormatter dtf = DateTimeFormatter.ofPattern("yyyy-MM-dd HH:mm:ss");

        try (BufferedWriter bw = new BufferedWriter(new FileWriter(fileName, true))) {
            while (true) {
                String input = scanner.nextLine();
                if (input.equalsIgnoreCase("exit")) break;
                bw.write(LocalDateTime.now().format(dtf) + " - " + input);
                bw.newLine();
            }
        } catch (IOException e) {
        }

        System.out.println("Logging stopped. Check user_log.txt");
        scanner.close();
    }
}
```

---

### OUTPUT:
<img width="929" height="386" alt="image" src="https://github.com/user-attachments/assets/04b05bac-4797-49cb-b6ba-30cce1107213" />


---

### RESULT:
Thus, the program successfully logs user input with timestamps into a text file.




