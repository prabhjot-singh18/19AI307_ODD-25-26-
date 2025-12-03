## Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY
 ### QUESTION:
Create animals from two regions: **Africa** and **Asia** using the **Abstract Factory Design Pattern**.  
Each region can create a family of animals (Herbivore & Carnivore).  
The carnivore must "eat" the herbivore and print the correct interaction.

Example:

Input:
```
africa
```

Output:
```
Lion eats Wildebeest
```

---

### AIM:
To implement the Abstract Factory design pattern in Java for creating region-specific families of animals and printing the interaction between carnivores and herbivores.

---

### ALGORITHM:

1. Create product interfaces: `Herbivore` and `Carnivore` with an `eat()` method in carnivore.  
2. Implement Africa animals: `Wildebeest` (Herbivore) and `Lion` (Carnivore).  
3. Implement Asia animals: `Buffalo` (Herbivore) and `Tiger` (Carnivore).  
4. Define an `AnimalFactory` abstract factory with methods to create herbivores and carnivores.  
5. Implement `AfricaFactory` and `AsiaFactory`.  
6. In `main()`, read the region name and instantiate the corresponding factory.  
7. Create animals through the factory and call `eat()` to print the interaction.

---

### PROGRAM:

```
Program to implement Abstract Factory Pattern for animal creation
Developed by: PRABHJOT SINGH
RegisterNumber: 212222040116
```

---

### Sourcecode.java:

```java
import java.util.Scanner;

// Abstract product interfaces
interface Herbivore {}
interface Carnivore {
    void eat(Herbivore h);
}

// Concrete Herbivores
class Wildebeest implements Herbivore {}
class Buffalo implements Herbivore {}

// Concrete Carnivores
class Lion implements Carnivore {
    public void eat(Herbivore h) {
        System.out.println("Lion eats Wildebeest");
    }
}

class Tiger implements Carnivore {
    public void eat(Herbivore h) {
        System.out.println("Tiger eats Buffalo");
    }
}

// Abstract Factory
interface AnimalFactory {
    Herbivore createHerbivore();
    Carnivore createCarnivore();
}

// Concrete Factories
class AfricaFactory implements AnimalFactory {
    public Herbivore createHerbivore() {
        return new Wildebeest();
    }
    public Carnivore createCarnivore() {
        return new Lion();
    }
}

class AsiaFactory implements AnimalFactory {
    public Herbivore createHerbivore() {
        return new Buffalo();
    }
    public Carnivore createCarnivore() {
        return new Tiger();
    }
}

// Client class
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String region = sc.nextLine().toLowerCase();
        AnimalFactory factory;

        if (region.equals("africa")) factory = new AfricaFactory();
        else if (region.equals("asia")) factory = new AsiaFactory();
        else {
            System.out.println("Invalid region");
            return;
        }

        Carnivore carn = factory.createCarnivore();
        Herbivore herb = factory.createHerbivore();
        carn.eat(herb);
    }
}
```

---

### OUTPUT:
<img width="707" height="247" alt="image" src="https://github.com/user-attachments/assets/5535465a-640f-433d-86c2-558f0b8904a1" />


---

### RESULT:
Thus, the Abstract Factory pattern was successfully used to create region-specific animal families and simulate their interaction.


