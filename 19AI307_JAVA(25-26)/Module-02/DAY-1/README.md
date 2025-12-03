## Ex.No:2(A) CLASS AND OBJECT
### QUESTION:
Create a class **City** with the following attributes:
- `cityName` (String)  
- `population` (long)  
- `area` (double)  

Create an object for the class and print all details.

Example:

Input:
```
New York
8419000
783.8
```

Output:
```
City Name: New York
Population: 8419000
Area: 783.8
```

---

### AIM:
To write a Java program that defines a class with attributes and creates an object to store and display city information.

---

### ALGORITHM:

1. Define a class `City` with attributes: cityName, population, and area.  
2. In the main method, create an object of the City class.  
3. Read input values from the user and assign them to the object attributes.  
4. Print all the attribute values of the object.  
5. End the program.

---

### PROGRAM:

```
Program to create a City class and print its details
Developed by: PRABHJOT SINGH
RegisterNumber: 212222040116
```

---

### Sourcecode.java:

```java
import java.util.*;

class City{
    String cityName;
    long population;
    double area;
}

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        City c = new City();
        
        c.cityName = sc.nextLine();
        c.population = sc.nextLong();
        c.area = sc.nextDouble();
        
        System.out.println("City Name: " + c.cityName);
        System.out.println("Population: " + c.population);
        System.out.println("Area: " + c.area);
    }
}
```

---

### OUTPUT:
<img width="703" height="389" alt="image" src="https://github.com/user-attachments/assets/81af8b3d-2f34-4e26-b96d-70c9af192654" />


---

### RESULT:
Thus, the Java program using a class and object to display city details was successfully executed.


