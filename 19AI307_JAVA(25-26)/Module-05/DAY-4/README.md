# Ex.No:5(D) THREAD PRIORITY
### QUESTION:
Write a Java program to determine the **priority** and **name** of the current thread.  
Read the thread name from the user and set it for the current thread.

Example:

Input:
```
NewThread
```

Output:
```
Priority of Thread: 5
Name of Thread: NewThread
Thread[NewThread,5,main]
```

---

### AIM:
To write a Java program that updates the current thread’s name and prints its name, priority, and full thread information.

---

### ALGORITHM:

1. Read the new thread name from the user.  
2. Get the reference to the current thread using `Thread.currentThread()`.  
3. Set the thread’s name using `setName()`.  
4. Retrieve the thread priority.  
5. Print the priority, name, and complete thread details.  

---

### PROGRAM:

```
Program to get and set current thread details
Developed by: PRABHJOT SINGH
RegisterNumber: 212222040116
```

---

### Sourcecode.java:

```java
import java.util.Scanner;

public class ThreadDetails {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String threadName = sc.nextLine();
        
        Thread currentThread = Thread.currentThread();
        
        currentThread.setName(threadName);
        
        // Get thread priority
        int priority = currentThread.getPriority();
        
        System.out.println("Priority of Thread: " + priority);
        System.out.println("Name of Thread: " + currentThread.getName());
        System.out.println(currentThread);
        
        sc.close();
    }
}
```

---

### OUTPUT:
<img width="730" height="207" alt="image" src="https://github.com/user-attachments/assets/be027702-17b5-488d-96f0-71bd45563146" />


---

### RESULT:
Thus, the program successfully retrieves and displays the current thread’s name, priority, and full thread information.



