# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION
### QUESTION:
Read **N numbers** from the user, then use a **fixed thread pool of size 3** to compute each number multiplied by 2.  
Return all results **in the same order as input**.

Example:

Input:
```
3
5
10
15
```

Output:
```
Result: 10
Result: 20
Result: 30
```

---

### AIM:
To write a Java program that uses a fixed thread pool (size 3) to process multiple tasks concurrently and return results in order using `Future`.

---

### ALGORITHM:

1. Read the number of tasks **T**.  
2. Create a fixed thread pool of size 3.  
3. For each number, submit a task that returns `"Result: <n*2>"`.  
4. Store futures in a list to preserve order.  
5. Retrieve and print results using `future.get()` in the same order.  
6. Shutdown the executor service.

---

### PROGRAM:

```
Program using fixed thread pool to compute n*2 for multiple inputs
Developed by: PAVAN KUMAR A B
RegisterNumber: 212222040113
```

---

### Sourcecode.java:

```java
import java.util.*;
import java.util.concurrent.*;

public class Main {
    public static void main(String[] args) throws Exception {
        Scanner sc = new Scanner(System.in);
        int T = Integer.parseInt(sc.nextLine());
        
        ExecutorService ex = Executors.newFixedThreadPool(3);
        List<Future<String>> futures = new ArrayList<>();

        for (int i = 0; i < T; i++) {
            int n = Integer.parseInt(sc.nextLine());
            futures.add(ex.submit(() -> "Result: " + (n * 2)));
        }

        for (Future<String> f : futures) {
            System.out.println(f.get());
        }

        ex.shutdown();
    }
}
```

---

### OUTPUT:
<img width="514" height="467" alt="image" src="https://github.com/user-attachments/assets/25654819-3656-4064-af18-f944f41c16fc" />

---

### RESULT:
Thus, the program successfully uses a fixed thread pool to process tasks concurrently and return ordered results.

