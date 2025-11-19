## Ex.No:1(B) CONDITIONAL STATEMENT

### QUESTION:
The "Publishers Federation Book Expo" is being held on the N-th floor of Hotel Grand Regency.  
Williams wants to reach the ground floor and can choose either the **stairs** or the **elevator**.

- Stairs are at a 45° angle, distance = √2 × N meters  
- Williams descends stairs at a speed of V1 m/s  
- The elevator starts at the ground floor, goes up to pick him, then goes down  
- Total elevator travel distance = 2 × N meters, speed = V2 m/s  

Determine whether **Stairs** or **Elevator** is faster.

Input: N, V1, V2  
Output: `"Stairs"` or `"Elevator"` depending on which option is quicker.

---

### AIM:
To write a Java program to compute and compare the time taken by stairs and elevator based on given distances and speeds, and determine the faster option.

---

### ALGORITHM:

1. Read the values of N, V1, and V2 from the user.  
2. Calculate the time taken using stairs using the formula: time = (√2 × N) / V1.  
3. Calculate the elevator time using the formula: time = (2 × N) / V2.  
4. Compare the two computed times.  
5. Display `"Stairs"` if stairs are faster, otherwise display `"Elevator"`.

---

### PROGRAM:

```
Program to determine the faster route (stairs or elevator)
Developed by: PAVAN KUMAR A B
RegisterNumber: 212222040113
```

---

### Sourcecode.java:

```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int N = sc.nextInt();
        int V1 = sc.nextInt();
        int V2 = sc.nextInt();

        double stairsTime = (Math.sqrt(2) * N) / V1;
        double elevatorTime = (2.0 * N) / V2;

        if (stairsTime < elevatorTime)
            System.out.println("Stairs");
        else
            System.out.println("Elevator");
    }
}
```

---

### OUTPUT:
<img width="454" height="209" alt="image" src="https://github.com/user-attachments/assets/fecd18fe-863e-41de-91b3-acbe3f9abe18" />



---

### RESULT:
Thus, the Java program to determine whether the stairs or elevator is faster was successfully executed.

