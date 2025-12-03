## Ex.No:2(C) ACCESS SPECIFIERS


### QUESTION:
Write a Java program to create a class **BankAccount** with private instance variables:  
- `accountNumber`  
- `balance`  

Provide public getter and setter methods to access and modify these variables.  
Create an object and print the details.

---

### AIM:
To write a Java program that demonstrates encapsulation using private variables and public getter/setter methods in a class.

---

### ALGORITHM:

1. Define a class `BankAccount` with private variables: accountNumber and balance.  
2. Provide public getter and setter methods for both variables.  
3. In the main method, create an object of `BankAccount`.  
4. Read the account number and balance from the user.  
5. Set the values using setter methods and print them using getter methods.

---

### PROGRAM:

```
Program to demonstrate encapsulation using getter and setter methods
Developed by: PRABHJOT SINGH
RegisterNumber: 212222040116
```

---

### Sourcecode.java:

```java
import java.util.Scanner;

class BankAccount {
    // Private instance variables
    private String accountNumber;
    private double balance;

    // Getter and Setter for accountNumber
    public String getAccountNumber() {
        return accountNumber;
    }
    public void setAccountNumber(String accountNumber) {
        this.accountNumber = accountNumber;
    }

    // Getter and Setter for balance
    public double getBalance() {
        return balance;
    }
    public void setBalance(double balance) {
        this.balance = balance;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        BankAccount account = new BankAccount();
        
        String accNum = sc.nextLine();
        account.setAccountNumber(accNum);

        double bal = sc.nextDouble();
        account.setBalance(bal);
        
        System.out.println("Account Number: " + account.getAccountNumber());
        System.out.println("Balance: " + account.getBalance());
    }
}
```

---

### OUTPUT:
<img width="950" height="377" alt="image" src="https://github.com/user-attachments/assets/ae9a93a6-5666-4be2-9193-df4990910efb" />


---

### RESULT:
Thus, the Java program demonstrating encapsulation using getter and setter methods was successfully executed.


