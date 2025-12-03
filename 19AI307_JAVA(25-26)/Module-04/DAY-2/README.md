## Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 
### QUESTION:
Simulate a print spooler system where **only one instance** of the Print Spooler Manager exists.  
Every department submitting a print job must use this single shared instance.  
Each job submitted increases the job count and logs the submission.

Example:

Input:
```
3
HR
Finance
IT
```

Output:
```
HR submitted a print job. Total Jobs in Queue: 1
Finance submitted a print job. Total Jobs in Queue: 2
IT submitted a print job. Total Jobs in Queue: 3
```

---

### AIM:
To implement a Singleton class in Java to ensure a single print spooler manager instance handles all print job submissions.

---

### ALGORITHM:

1. Create a class `PrintSpoolerManager` with a private static instance variable.  
2. Make the constructor private to prevent outside instantiation.  
3. Provide a static `getInstance()` method to return the one shared object.  
4. Maintain a counter for total print jobs.  
5. Accept department names and submit print jobs through the singleton object.  
6. Print the department name and updated job count for each submission.

---

### PROGRAM:

```
Program to simulate a singleton print spooler job manager
Developed by: PRABHJOT SINGH
RegisterNumber: 212222040116
```

---

### Sourcecode.java:

```java
import java.util.*;

class PrintSpoolerManager {
    private static PrintSpoolerManager instance;  
    private int jobCount;                         

    private PrintSpoolerManager() {
        jobCount = 0;
    }

    public static PrintSpoolerManager getInstance() {
        if (instance == null) {
            instance = new PrintSpoolerManager();
        }
        return instance;
    }

    public void submitJob(String department) {
        jobCount++;
        System.out.println(department + " submitted a print job. Total Jobs in Queue: " + jobCount);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        int n = Integer.parseInt(sc.nextLine());
        PrintSpoolerManager spooler = PrintSpoolerManager.getInstance();

        for (int i = 0; i < n; i++) {
            String department = sc.nextLine();
            spooler.submitJob(department);
        }

        sc.close();
    }
}
```

---

### OUTPUT:
<img width="1188" height="438" alt="image" src="https://github.com/user-attachments/assets/ace7243f-6fb6-4537-b39d-4c1f36c696f8" />


---

### RESULT:
Thus, the Java program successfully implemented a singleton print spooler manager that maintains a shared job count across all accesses.


