# Ex.No:5(C)  FILE HANDLING USING JAVA
### QUESTION:
Write a Java program to count the number of words in a file.  
The program should first write user input into a file and then read it back to count the words.

Example:

Input:
```
Java is a powerful programming language
```

Output:
```
Number of words in the file: 6
```

---

### AIM:
To write a Java program that stores user input in a file, reads the file, and counts the number of words present in it.

---

### ALGORITHM:

1. Read a full line of text from the user.  
2. Write this text into a file (`userwords.txt`).  
3. Reopen the file for reading.  
4. Use a `Scanner` to read tokens (words) one by one.  
5. Increment a counter for each word.  
6. Display the final word count.

---

### PROGRAM:

```
Program to count number of words in a text file
Developed by: PRABHJOT SINGH
RegisterNumber: 212222040116
```

---

### Sourcecode.java:

```java
import java.io.FileWriter;
import java.io.FileReader;
import java.io.IOException;
import java.util.Scanner;

public class CountWordsInFile {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String fileName = "userwords.txt";

        String input = scanner.nextLine();

        // Step 1: Write user input to file
        try {
            FileWriter writer = new FileWriter(fileName);
            writer.write(input);
            writer.close();
        } catch (IOException e) {
            System.out.println("Error writing to the file.");
            e.printStackTrace();
            scanner.close();
            return;
        }

        // Step 2: Read from file and count words
        int wordCount = 0;
        try {
            FileReader reader = new FileReader(fileName);
            Scanner fileScanner = new Scanner(reader);

            while (fileScanner.hasNext()) {
                fileScanner.next();
                wordCount++;
            }

            fileScanner.close();
            reader.close();
        } catch (IOException e) {
            System.out.println("Error reading the file.");
            e.printStackTrace();
        }

        System.out.println("Number of words in the file: " + wordCount);
        scanner.close();
    }
}
```

---

### OUTPUT:
<img width="1096" height="248" alt="image" src="https://github.com/user-attachments/assets/a0145df4-12f0-4166-ab60-b274eecfca11" />


---

### RESULT:
Thus, the program successfully counts the number of words written into a file.



