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
## Here's an implementation of the OrderingSystem and Salad classes based on the requirements listed:
1. Your application will have two classes –an OrderingSystem class with a main method and a Salad class
that will serve as a blueprint to create a new salad for the customer.
2. Create your Salad class. Add attributes to hold the type of greens, the type of protein, and the toppings
the customer specifies. Add an attribute called isVegan to track if the salad is vegan or not. Add a
constructor and the accessor methods (getters and setters.)
3. Create an Ordering system class with a main method. Add the code for the remaining requirements to
the main method.
4. Declare a variable to hold the STG greeting: “Welcome to Salads to Go!”
5. Declare a variable to hold the STG slogan: “Build Your Own Salads, Your Way. Time to build a salad.”
6. Declare a Boolean variable called “isVegan”. (We will use this variable to track whether the user’s salad
order is vegan or not.)
7. Declare three ArrayLists to hold the types of greens, types of proteins, and types of toppings. Populate
the lists with the values below.
a. Greens types: kale, romaine lettuce, iceberg lettuce
b. Proteins: tuna, chicken, or black beans
c. Toppings: cheese, croutons, tomatoes, onions, bacon, and olives
8. Add a method to the application that displays the greens types, proteins, and toppings to the customer.
Within the method, use a loop to iterate over the items in the list and display them to the customer.
9. Display the greeting and the slogan to the customer.
10. Call the method to display the greens types to the customer.
11. Then prompt the customer to choose a type of salad greens by asking “What type of salad greens do you
want?”
12. Create a new salad object and with the type of greens the customer has chosen.
13. Call the method to display the proteins to the customer.
14. Prompt the customer to choose a type of protein by asking “What type of protein do you want?”
---

```csharp
//CSHARP
import java.util.ArrayList;
import java.util.Scanner;

public class OrderingSystem {
    public static void main(String[] args) {
        String greeting = "Welcome to Salads to Go!";
        String slogan = "Build Your Own Salads, Your Way. Time to build a salad.";
        Boolean isVegan;
        ArrayList<String> greens = new ArrayList<>();
        greens.add("kale");
        greens.add("romaine lettuce");
        greens.add("iceberg lettuce");
        ArrayList<String> proteins = new ArrayList<>();
        proteins.add("tuna");
        proteins.add("chicken");
        proteins.add("black beans");
        ArrayList<String> toppings = new ArrayList<>();
        toppings.add("cheese");
        toppings.add("croutons");
        toppings.add("tomatoes");
        toppings.add("onions");
        toppings.add("bacon");
        toppings.add("olives");
        
        // Display greeting and slogan
        System.out.println(greeting);
        System.out.println(slogan);
        
        // Display greens types
        System.out.println("Greens:");
        for (String green : greens) {
            System.out.println("- " + green);
        }
        
        // Prompt customer for type of greens
        Scanner scanner = new Scanner(System.in);
        System.out.print("What type of salad greens do you want? ");
        String greensChoice = scanner.nextLine();
        
        // Create new salad object with chosen greens
        Salad salad = new Salad(greensChoice);
        
        // Display protein types
        System.out.println("Proteins:");
        for (String protein : proteins) {
            System.out.println("- " + protein);
        }
        
        // Prompt customer for type of protein
        System.out.print("What type of protein do you want? ");
        String proteinChoice = scanner.nextLine();
        
        // Set protein choice for salad
        salad.setProtein(proteinChoice);
        
        // Display toppings
        System.out.println("Toppings:");
        for (String topping : toppings) {
            System.out.println("- " + topping);
        }
        
        // Prompt customer for toppings
        System.out.print("What toppings do you want? ");
        String toppingsChoice = scanner.nextLine();
        
        // Set toppings for salad
        salad.setToppings(toppingsChoice);
        
        // Determine if salad is vegan based on protein choice
        isVegan = salad.getProtein().equals("black beans");
        salad.setIsVegan(isVegan);
        
        // Display salad order
        System.out.println("You ordered a salad with " + salad.getGreens() + ", " +
                           salad.getProtein() + ", and " + salad.getToppings() + ".");
        if (isVegan) {
            System.out.println("This salad is vegan.");
        } else {
            System.out.println("This salad is not vegan.");
        }
    }
}

public class Salad {
    private String greens;
    private String protein;
    private String toppings;
    private Boolean isVegan;
    
    public Salad(String greens) {
        this.greens = greens;
    }
    
    public String getGreens() {
        return greens;
    }
    
    public void setGreens(String greens) {
        this.greens = greens;
    }
    
    public String getProtein() {
        return protein;
    }
    
    public void setProtein(String protein) {
        this.protein = protein;
    }
    
    public String getToppings() {
        return toppings;
    }
    
    public void setToppings(String toppings) {
        this.toppings = toppings

```
---
// TYPESCRIPT

```typescript
public class OrderingSystem {
    public static void main(String[] args) {
        // Code for the ordering system
    }
}

public class Salad {
    private String greensType;
    private String proteinType;
    private ArrayList<String> toppings;
    private boolean isVegan;

    public Salad(String greensType) {
        this.greensType = greensType;
        this.toppings = new ArrayList<String>();
    }

    public String getGreensType() {
        return greensType;
    }

    public void setGreensType(String greensType) {
        this.greensType = greensType;
    }

    public String getProteinType() {
        return proteinType;
    }

    public void setProteinType(String proteinType) {
        this.proteinType = proteinType;
    }

    public ArrayList<String> getToppings() {
        return toppings;
    }

    public void setToppings(ArrayList<String> toppings) {
        this.toppings = toppings;
    }

    public boolean isVegan() {
        return isVegan;
    }

    public void setVegan(boolean isVegan) {
        this.isVegan = isVegan;
    }
}

```
---
