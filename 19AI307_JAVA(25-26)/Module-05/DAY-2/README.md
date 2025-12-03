# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 
### QUESTION:
Write a Java program to serialize a collection of objects (such as an `ArrayList<Student>`) into a file and then deserialize it back.

Example:

Input:
```
2
101
Alice
89.5
102
Bob
92.0
```

Output:
```
Students serialized successfully into: students.dat
Students deserialized successfully from: students.dat

Deserialized Students:
Student{id=101, name='Alice', marks=89.5}
Student{id=102, name='Bob', marks=92.0}
```

---

### AIM:
To write a Java program that serializes and deserializes a list of `Student` objects using `ObjectOutputStream` and `ObjectInputStream`.

---

### ALGORITHM:

1. Create a `Student` class that implements `Serializable`.  
2. Read user input and populate an `ArrayList<Student>`.  
3. Serialize the student list into a `.dat` file.  
4. Deserialize the list back from the file.  
5. Display the deserialized student objects.

---

### PROGRAM:

```
Program to serialize and deserialize a list of Student objects
Developed by: PRABHJOT SINGH
RegisterNumber: 212222040116
```

---

### Sourcecode.java:

```java
import java.io.*;
import java.util.*;

// Student class must implement Serializable
class Student implements Serializable {
    private static final long serialVersionUID = 1L;

    private int id;
    private String name;
    private double marks;

    public Student(int id, String name, double marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }

    @Override
    public String toString() {
        return "Student{id=" + id + ", name='" + name + "', marks=" + marks + "}";
    }
}

public class StudentSerializationUserInput {

    // Serialize list of students
    public static void serializeStudents(List<Student> students, String fileName) {
        try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream(fileName))) {
            oos.writeObject(students);
            System.out.println("Students serialized successfully into: " + fileName);
        } catch (IOException e) {
            System.out.println("Error during serialization: " + e.getMessage());
        }
    }

    // Deserialize list of students
    @SuppressWarnings("unchecked")
    public static List<Student> deserializeStudents(String fileName) {
        List<Student> students = null;
        try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream(fileName))) {
            students = (List<Student>) ois.readObject();
            System.out.println("Students deserialized successfully from: " + fileName);
        } catch (IOException | ClassNotFoundException e) {
            System.out.println("Error during deserialization: " + e.getMessage());
        }
        return students;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        List<Student> students = new ArrayList<>();

        int n = scanner.nextInt();
        scanner.nextLine(); // consume newline

        for (int i = 0; i < n; i++) {
            int id = scanner.nextInt();
            scanner.nextLine(); // consume newline
            String name = scanner.nextLine();
            double marks = scanner.nextDouble();
            scanner.nextLine(); // consume newline

            students.add(new Student(id, name, marks));
        }

        String fileName = "students.dat";

        // Serialize
        serializeStudents(students, fileName);

        // Deserialize
        List<Student> deserializedStudents = deserializeStudents(fileName);

        // Display deserialized data
        if (deserializedStudents != null) {
            System.out.println("\nDeserialized Students:");
            for (Student s : deserializedStudents) {
                System.out.println(s);
            }
        }

        scanner.close();
    }
}
```

---

### OUTPUT:
<img width="1186" height="582" alt="image" src="https://github.com/user-attachments/assets/11de1e65-855c-4eb8-8fe7-c93d600b958c" />


---

### RESULT:
Thus, the program successfully serialized and deserialized a list of student objects using Java’s object streams.



