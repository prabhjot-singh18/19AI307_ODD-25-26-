## Ex.No:3(A) INHERITANCE AND AGGREGATION

### QUESTION:
A jewelry store tracks gold rates for different customer types. The base class `Customer` has attributes: `customerId`, `name`, and `purchaseWeight` (grams).  
There are two derived types: `RegularCustomer` (2% discount on gold rate per gram) and `PremiumCustomer` (5% discount + cashback of 1% of the final price). The base gold rate per gram is input at runtime.

For each customer, calculate and display the final price:
```
finalPrice = purchaseWeight * (goldRatePerGram - discountAmountPerGram)
```
For PremiumCustomer also display the cashback amount (1% of finalPrice).

**Input (example order):**
- Customer type (Regular or Premium)  
- customerId  
- name  
- purchaseWeight (double)  
- goldRatePerGram (double)

**Output:** display customer details, discount percent, final price, and cashback for premium customers.

---

### AIM:
To write a Java program that demonstrates inheritance and polymorphism by computing final gold purchase price for Regular and Premium customers, applying discounts and cashback where applicable.

---

### ALGORITHM:

1. Define a base class `Customer` with attributes: customerId, name, purchaseWeight, and goldRatePerGram; include methods to compute discount rate, final price, and display details.  
2. Create `RegularCustomer` that overrides the discount rate method to return 2%.  
3. Create `PremiumCustomer` that overrides the discount rate to return 5% and adds a method to compute cashback as 1% of final price.  
4. In `main`, read input (type, id, name, weight, rate), instantiate the appropriate subclass based on type, and call its `display()` method.  
5. `display()` should print formatted customer details, discount %, final price (2 decimal places) and cashback (for premium customers).

---

### PROGRAM:
```
Program to calculate final price for customers with discounts and cashback
Developed by: PRABHJOT SINGH
RegisterNumber: 212222040116
```

---

### Sourcecode.java:

```java
import java.util.*;
import java.text.DecimalFormat;

class Customer {
    String customerId, name;
    double purchaseWeight, goldRatePerGram;

    Customer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        this.customerId = customerId;
        this.name = name;
        this.purchaseWeight = purchaseWeight;
        this.goldRatePerGram = goldRatePerGram;
    }

    double getDiscountRate() {
        return 0;
    }

    double calculateFinalPrice() {
        double discountAmount = goldRatePerGram * getDiscountRate() / 100;
        double effectiveRate = goldRatePerGram - discountAmount;
        return purchaseWeight * effectiveRate;
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: General");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}

class RegularCustomer extends Customer {
    RegularCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    double getDiscountRate() {
        return 2.0;
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Regular");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}

class PremiumCustomer extends Customer {
    PremiumCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    double getDiscountRate() {
        return 5.0;
    }

    double getCashback() {
        return calculateFinalPrice() * 0.01;
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Premium");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
        System.out.println("Cashback: " + df.format(getCashback()));
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String type = sc.nextLine().trim();   // Regular or Premium
        String id = sc.nextLine().trim();
        String name = sc.nextLine().trim();
        double weight = Double.parseDouble(sc.nextLine().trim());
        double rate = Double.parseDouble(sc.nextLine().trim());

        Customer c;
        if (type.equalsIgnoreCase("Regular")) {
            c = new RegularCustomer(id, name, weight, rate);
        } else {
            c = new PremiumCustomer(id, name, weight, rate);
        }
        c.display();
    }
}
```

---

### OUTPUT:
<img width="1052" height="706" alt="image" src="https://github.com/user-attachments/assets/78e5e6d3-2d6d-43e0-bf14-aa57e8fcba0a" />


---

### RESULT:
Thus, the Java program demonstrating inheritance and polymorphism to compute discounted gold prices and cashback was successfully executed.

