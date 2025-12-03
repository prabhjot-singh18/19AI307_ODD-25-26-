## Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR
### QUESTION:
Create a Java class **Book** with instance variables:
- `title`
- `author`

Read the values from the user, create an object using a constructor, and print the book details.

Example:

Input:
```
C programming
Dennis Ritchie
```

Output:
```
Book Title: C programming
Author: Dennis Ritchie
```

---

### AIM:
To write a Java program that defines a class with a parameterized constructor and creates an object to display book details.

---

### ALGORITHM:

1. Define a class `Book` with instance variables: title and author.  
2. Create a parameterized constructor to initialize these variables.  
3. In the main method, read the book title and author from the user.  
4. Create an object of the Book class using the constructor.  
5. Print the values of title and author.

---

### PROGRAM:

```
Program to create a Book class and display its details using a constructor
Developed by: PRABHJOT SINGH
RegisterNumber: 212222040116
```

---

### Sourcecode.java:

```java
import java.util.*;

public class Book{
    String title, author;
    
    Book(String title, String author){
        this.title = title;
        this.author = author;
    }
    
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        
        String tit = sc.nextLine();
        String aut = sc.nextLine();
        
        Book b = new Book(tit, aut);
        
        System.out.println("Book Title: " + b.title);
        System.out.println("Author: " + b.author);
    }
}
```

---

### OUTPUT:
<img width="889" height="311" alt="image" src="https://github.com/user-attachments/assets/8e13adf8-0c68-4c44-9568-da14df521505" />


---

### RESULT:
Thus, the Java program using a parameterized constructor to display book details was successfully executed.





