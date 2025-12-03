## Ex.No:3(b) POLYMORPHISM
### QUESTION:
Write a Java program to:

- Create a base class **Shape** with methods `draw()` and `calculateArea()`.
- Create two subclasses:
  - **Circle**: overrides `draw()` and `calculateArea()`  
  - **Cylinder**: overrides `draw()` and `calculateArea()` to compute **total surface area**
- Accept user input to choose between circle and cylinder and read the required dimensions.
- Display the drawing message and the computed area.

Example:

Input:
```
circle
5
```

Output:
```
Drawing a circle...
Area: 78.54
```

---

### AIM:
To write a Java program demonstrating inheritance and method overriding by implementing shape-specific drawing and area calculations for circles and cylinders.

---

### ALGORITHM:

1. Create a base class `Shape` with the methods `draw()` and `calculateArea()`.  
2. Define the subclass `Circle` that overrides both methods to compute the area of a circle.  
3. Define the subclass `Cylinder` that overrides the methods and calculates the cylinder’s total surface area.  
4. In `main()`, read the shape type and required dimensions from the user.  
5. Create the appropriate Shape object, call its `draw()` method, and print the area with two-decimal formatting.

---

### PROGRAM:

```
Program to demonstrate inheritance and method overriding (circle & cylinder)
Developed by: PRABHJOT SINGH
RegisterNumber: 212222040116
```

---

### Sourcecode.java:

```java
import java.util.*;

class Shape {
    void draw() {}
    double calculateArea() { return 0; }
}

class Circle extends Shape {
    double radius;
    Circle(double radius) {
        this.radius = radius;
    }
    void draw() {
        System.out.println("Drawing a circle...");
    }
    double calculateArea() {
        return Math.PI * radius * radius;
    }
}

class Cylinder extends Shape {
    double radius, height;
    Cylinder(double radius, double height) {
        this.radius = radius;
        this.height = height;
    }
    void draw() {
        System.out.println("Drawing a cylinder...");
    }
    double calculateArea() {
        return 2 * Math.PI * radius * (radius + height);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        String type = sc.nextLine().toLowerCase();
        Shape s;
        
        if (type.equals("circle")) {
            double r = sc.nextDouble();
            s = new Circle(r);
        } else if (type.equals("cylinder")) {
            double r = sc.nextDouble();
            double h = sc.nextDouble();
            s = new Cylinder(r, h);
        } else {
            System.out.println("Invalid shape type.");
            return;
        }
        
        s.draw();
        System.out.printf("Area: %.2f", s.calculateArea());
    }
}
```

---

### OUTPUT:
<img width="731" height="310" alt="image" src="https://github.com/user-attachments/assets/c0ac878d-5418-44df-a7d9-0a5850435580" />


---

### RESULT:
Thus, the Java program using inheritance and method overriding to compute areas of shapes (circle & cylinder) was successfully executed.


