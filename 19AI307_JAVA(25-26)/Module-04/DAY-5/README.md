# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN
### QUESTION:
Build a simple Air Traffic Control System where multiple `Airplane` objects request landing through a central mediator.

Each airplane requests landing, and the mediator decides based on runway availability.  
Only the first airplane is allowed to land when the runway is busy.

Example:

Input:
```
3
true
AirIndia101
SpiceJet505
Indigo303
```

Output:
```
AirIndia101 granted landing.
AirIndia101 landed successfully.
SpiceJet505 granted landing.
SpiceJet505 landed successfully.
Indigo303 granted landing.
Indigo303 landed successfully.
```

---

### AIM:
To implement the Mediator Design Pattern using an Air Traffic Control system that manages landing requests from airplanes.

---

### ALGORITHM:

1. Define the `AirTrafficControl` interface with `requestLanding()`.  
2. Implement the `ATCMediator` class to control landing permissions.  
3. Create an `Airplane` class that interacts with the mediator.  
4. Mark the first airplane as priority when the runway is busy.  
5. Read input, create mediator and airplane objects, and process landing requests.

---

### PROGRAM:

```
Program to simulate Air Traffic Control using Mediator Pattern
Developed by: PRABHJOT SINGH
RegisterNumber: 212222040116
```

---

### Sourcecode.java:

```java
import java.util.*;

interface AirTrafficControl {
    void requestLanding(Airplane airplane);
}

class ATCMediator implements AirTrafficControl {
    private boolean isRunwayFree;

    public ATCMediator(boolean isRunwayFree) {
        this.isRunwayFree = isRunwayFree;
    }

    @Override
    public void requestLanding(Airplane airplane) {
        if (isRunwayFree) {
            System.out.println(airplane.getName() + " granted landing.");
            airplane.land();
        } else {
            if (airplane.isFirst()) {
                System.out.println(airplane.getName() + " granted landing.");
                airplane.land();
            } else {
                System.out.println(airplane.getName() + " denied landing. Runway busy.");
            }
        }
    }
}

class Airplane {
    private String name;
    private AirTrafficControl atc;
    private boolean first;

    public Airplane(String name, AirTrafficControl atc, boolean first) {
        this.name = name;
        this.atc = atc;
        this.first = first;
    }

    public String getName() {
        return name;
    }

    public boolean isFirst() {
        return first;
    }

    public void requestLanding() {
        atc.requestLanding(this);
    }

    public void land() {
        System.out.println(name + " landed successfully.");
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        while (sc.hasNextInt()) {
            int n = sc.nextInt();
            boolean runwayStatus = sc.nextBoolean();
            sc.nextLine(); // consume newline

            ATCMediator mediator = new ATCMediator(runwayStatus);
            List<Airplane> airplanes = new ArrayList<>();

            for (int i = 0; i < n; i++) {
                String name = sc.nextLine().trim();
                airplanes.add(new Airplane(name, mediator, i == 0));
            }

            for (Airplane airplane : airplanes) {
                airplane.requestLanding();
            }
        }

        sc.close();
    }
}
```

---

### OUTPUT:
<img width="1057" height="537" alt="image" src="https://github.com/user-attachments/assets/264a1cf6-3478-4013-bc85-ed6eb07e4f7a" />


---

### RESULT:
Thus, the Mediator Pattern was successfully used to coordinate airplane landings through a single Air Traffic Control mediator.


