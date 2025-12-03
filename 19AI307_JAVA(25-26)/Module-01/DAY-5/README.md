## Ex.No:4 FINDING THE LONGEST WORD IN A SENTENCE

### QUESTION:
Write a Java program to read a sentence and determine the longest word present in it.

Example:

Input:  
```
Apple Orange
```
Output:  
```
The longest word is: Orange
```

---

### AIM:
To write a Java program that processes a sentence, splits it into words, and identifies the longest word among them.

---

### ALGORITHM:

1. Read the entire sentence as a string input from the user.  
2. Split the sentence into individual words using whitespace as the delimiter.  
3. Initialize a variable to store the longest word found so far.  
4. Compare the length of each word with the current longest word and update when necessary.  
5. Display the longest word.

---

### PROGRAM:

```
Program to find the longest word in a given sentence
Developed by: PRABHJOT SINGH
RegisterNumber: 212222040116
```

---

### Sourcecode.java:

```java
import java.util.*;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        String sen = sc.nextLine();
        
        String[] words = sen.split("\\s+");
        String longestWord = "";
        
        for(String word : words){
            if(word.length() > longestWord.length()){
                longestWord = word;
            }
        }
        
        System.out.print("The longest word is: " + longestWord); 
        sc.close();
    }
}
```

---

### OUTPUT:
<img width="829" height="254" alt="image" src="https://github.com/user-attachments/assets/2048dfc1-020e-4e9b-8afd-0a119503533b" />


---

### RESULT:
Thus, the Java program to find the longest word in a sentence was successfully executed.


