# chatGPT.Menu
## Experiment with chatGPT to generate Java code for a fast-food restaurant menu 
---

Here is an example Java program for a fast food menu:
---
---


```java
//JAVA 
import java.util.Scanner;

public class FastFoodMenu {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int choice;
        
        System.out.println("Welcome to Fast Food Restaurant");
        System.out.println("Please choose an item from our menu:");
        System.out.println("1. Hamburger - $5.00");
        System.out.println("2. Cheeseburger - $6.00");
        System.out.println("3. Chicken sandwich - $7.00");
        System.out.println("4. French fries - $3.00");
        System.out.println("5. Onion rings - $4.00");
        
        System.out.print("Enter your choice (1-5): ");
        choice = scanner.nextInt();
        
        switch (choice) {
            case 1:
                System.out.println("You ordered a hamburger. That will be $5.00.");
                break;
            case 2:
                System.out.println("You ordered a cheeseburger. That will be $6.00.");
                break;
            case 3:
                System.out.println("You ordered a chicken sandwich. That will be $7.00.");
                break;
            case 4:
                System.out.println("You ordered french fries. That will be $3.00.");
                break;
            case 5:
                System.out.println("You ordered onion rings. That will be $4.00.");
                break;
            default:
                System.out.println("Invalid choice. Please enter a number between 1 and 5.");
                break;
        }
        
        scanner.close();
    }
}

---
---


```php
//PHP 
import java.util.Scanner;

public class FastFoodMenu {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int choice;
        
        do {
            System.out.println("Welcome to the Fast Food Menu");
            System.out.println("1. Hamburger - $4.99");
            System.out.println("2. Cheeseburger - $5.49");
            System.out.println("3. Chicken sandwich - $6.99");
            System.out.println("4. Fries - $2.49");
            System.out.println("5. Soda - $1.49");
            System.out.println("6. Quit");
            System.out.print("Enter your choice (1-6): ");
            choice = scanner.nextInt();
            
            switch (choice) {
                case 1:
                    System.out.println("You ordered a Hamburger. That will be $4.99.");
                    break;
                case 2:
                    System.out.println("You ordered a Cheeseburger. That will be $5.49.");
                    break;
                case 3:
                    System.out.println("You ordered a Chicken sandwich. That will be $6.99.");
                    break;
                case 4:
                    System.out.println("You ordered Fries. That will be $2.49.");
                    break;
                case 5:
                    System.out.println("You ordered a Soda. That will be $1.49.");
                    break;
                case 6:
                    System.out.println("Goodbye!");
                    break;
                default:
                    System.out.println("Invalid choice. Please try again.");
            }
            
            System.out.println();
        } while (choice != 6);
    }
}
```
---
