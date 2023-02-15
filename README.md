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
//TYPESCRIPT
```typescript
public class OrderingSystem {
    public static void main(String[] args) {
        // add code here
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
    
    // accessor methods
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
        if (proteinType.equals("tuna") || proteinType.equals("chicken")) {
            isVegan = false;
        } else {
            isVegan = true;
        }
    }
    
    public ArrayList<String> getToppings() {
        return toppings;
    }
    
    public void addTopping(String topping) {
        toppings.add(topping);
        if (topping.equals("cheese") || topping.equals("bacon")) {
            isVegan = false;
        } else {
            isVegan = true;
        }
    }
    
    public boolean isVegan() {
        return isVegan;
    }
}

```
---
```csharp
//CSHARP

public class OrderingSystem {
    public static void main(String[] args) {
        String greeting = "Welcome to Salads to Go!";
        String slogan = "Build Your Own Salads, Your Way. Time to build a salad.";
        boolean isVegan;
        
        // initialize lists
        ArrayList<String> greensTypes = new ArrayList<String>();
        greensTypes.add("kale");
        greensTypes.add("romaine lettuce");
        greensTypes.add("iceberg lettuce");
        
        ArrayList<String> proteinTypes = new ArrayList<String>();
        proteinTypes.add("tuna");
        proteinTypes.add("chicken");
        proteinTypes.add("black beans");
        
        ArrayList<String> toppingTypes = new ArrayList<String>();
        toppingTypes.add("cheese");
        toppingTypes.add("croutons");
        toppingTypes.add("tomatoes");
        toppingTypes.add("onions");
        toppingTypes.add("bacon");
        toppingTypes.add("olives");
        
        // display options
        displayOptions(greensTypes, "salad greens");
        displayOptions(proteinTypes, "protein");
        displayOptions(toppingTypes, "topping");
        
        // get greens type from user
        Scanner scanner = new Scanner(System.in);
        System.out.println("What type of salad greens do you want?");
        String greensType = scanner.nextLine();
        
        // create new salad object
        Salad salad = new Salad(greensType);
        
        // get protein type from user
        System.out.println("What type of protein do you want?");
        String proteinType = scanner.nextLine();
        salad.setProteinType(proteinType);
        
        // get toppings from user
        ArrayList<String> toppings = new ArrayList<String>();
        while (true) {
            System.out.println("What type of topping do you want? (Enter 'done' to finish)");
            String topping = scanner.nextLine();
            if (topping.equals("done")) {
                break;
            }
            salad.addTopping(topping);
        }
        
        // display salad information
        System.out.println("You ordered a " + salad.getProteinType() + " salad on " + salad.getGreensType() + ".");
        if

```
---
```java 

import java.util.ArrayList;
import java.util.Scanner;

public class OrderingSystem {
public static void main(String[] args) {
String greeting = "Welcome to Salads to Go!";
String slogan = "Build Your Own Salads, Your Way. Time to build a salad.";
boolean isVegan;

    // initialize lists
    ArrayList<String> greensTypes = new ArrayList<String>();
    greensTypes.add("kale");
    greensTypes.add("romaine lettuce");
    greensTypes.add("iceberg lettuce");
    
    ArrayList<String> proteinTypes = new ArrayList<String>();
    proteinTypes.add("tuna");
    proteinTypes.add("chicken");
    proteinTypes.add("black beans");
    
    ArrayList<String> toppingTypes = new ArrayList<String>();
    toppingTypes.add("cheese");
    toppingTypes.add("croutons");
    toppingTypes.add("tomatoes");
    toppingTypes.add("onions");
    toppingTypes.add("bacon");
    toppingTypes.add("olives");
    
    // display options
    displayOptions(greensTypes, "salad greens");
    displayOptions(proteinTypes, "protein");
    displayOptions(toppingTypes, "topping");
    
    // get greens type from user
    Scanner scanner = new Scanner(System.in);
    System.out.println("What type of salad greens do you want?");
    String greensType = scanner.nextLine();
    
    // create new salad object
    Salad salad = new Salad(greensType);
    
    // get protein type from user
    System.out.println("What type of protein do you want?");
    String proteinType = scanner.nextLine();
    salad.setProteinType(proteinType);
    
    // get toppings from user
    ArrayList<String> toppings = new ArrayList<String>();
    while (true) {
        System.out.println("What type of topping do you want? (Enter 'done' to finish)");
        String topping = scanner.nextLine();
        if (topping.equals("done")) {
            break;
        }
        salad.addTopping(topping);
    }
    
    // display salad information
    System.out.println("You ordered a " + salad.getProteinType() + " salad on " + salad.getGreensType() + ".");
}

public static void displayOptions(ArrayList<String> options, String type) {
    System.out.println("Choose a " + type + ":");
    for (int i = 0; i < options.size(); i++) {
        System.out.println(i+1 + ". " + options.get(i));
    }
}

```
---
```java
//JAVA

import java.util.ArrayList;
import java.util.Scanner;

public class OrderingSystem {
public static void main(String[] args) {
String greeting = "Welcome to Salads to Go!";
String slogan = "Build Your Own Salads, Your Way. Time to build a salad.";
boolean isVegan;
    // initialize lists
    ArrayList<String> greensTypes = new ArrayList<String>();
    greensTypes.add("kale");
    greensTypes.add("romaine lettuce");
    greensTypes.add("iceberg lettuce");

    ArrayList<String> proteinTypes = new ArrayList<String>();
    proteinTypes.add("tuna");
    proteinTypes.add("chicken");
    proteinTypes.add("black beans");

    ArrayList<String> toppingTypes = new ArrayList<String>();
    toppingTypes.add("cheese");
    toppingTypes.add("croutons");
    toppingTypes.add("tomatoes");
    toppingTypes.add("onions");
    toppingTypes.add("bacon");
    toppingTypes.add("olives");

    // display options
    displayOptions(greensTypes, "salad greens");
    displayOptions(proteinTypes, "protein");
    displayOptions(toppingTypes, "topping");

    // get greens type from user
    Scanner scanner = new Scanner(System.in);
    System.out.println("What type of salad greens do you want?");
    String greensType = scanner.nextLine();

    // create new salad object
    Salad salad = new Salad(greensType);

    // get protein type from user
    System.out.println("What type of protein do you want?");
    String proteinType = scanner.nextLine();
    salad.setProteinType(proteinType);

    // get toppings from user
    ArrayList<String> toppings = new ArrayList<String>();
    while (true) {
        System.out.println("What type of topping do you want? (Enter 'done' to finish)");
        String topping = scanner.nextLine();
        if (topping.equals("done")) {
            break;
        }
        salad.addTopping(topping);
    }

    // display salad information
    System.out.println("You ordered a " + salad.getProteinType() + " salad on " + salad.getGreensType() + ".");
}

public static void displayOptions(ArrayList<String> options, String category) {
    System.out.println("Choose your " + category + ":");
    for (String option : options) {
        System.out.println("- " + option);
    }
}

    // initialize lists
    ArrayList<String> greensTypes = new ArrayList<String>();
    greensTypes.add("kale");
    greensTypes.add("romaine lettuce");
    greensTypes.add("iceberg lettuce");

    ArrayList<String> proteinTypes = new ArrayList<String>();
    proteinTypes.add("tuna");
    proteinTypes.add("chicken");
    proteinTypes.add("black beans");

    ArrayList<String> toppingTypes = new ArrayList<String>();
    toppingTypes.add("cheese");
    toppingTypes.add("croutons");
    toppingTypes.add("tomatoes");
    toppingTypes.add("onions");
    toppingTypes.add("bacon");
    toppingTypes.add("olives");

    // display options
    displayOptions(greensTypes, "salad greens");
    displayOptions(proteinTypes, "protein");
    displayOptions(toppingTypes, "topping");

    // get greens type from user
    Scanner scanner = new Scanner(System.in);
    System.out.println("What type of salad greens do you want?");
    String greensType = scanner.nextLine();

    // create new salad object
    Salad salad = new Salad(greensType);

    // get protein type from user
    System.out.println("What type of protein do you want?");
    String proteinType = scanner.nextLine();
    salad.setProteinType(proteinType);

    // get toppings from user
    ArrayList<String> toppings = new ArrayList<String>();
    while (true) {
        System.out.println("What type of topping do you want? (Enter 'done' to finish)");
        String topping = scanner.nextLine();
        if (topping.equals("done")) {
            break;
        }
        salad.addTopping(topping);
    }

    // display salad information
    System.out.println("You ordered a " + salad.getProteinType() + " salad on " + salad.getGreensType() + ".");
}

public static void displayOptions(ArrayList<String> options, String category) {
    System.out.println("Choose your " + category + ":");
    for (String option : options) {
        System.out.println("- " + option);
    }
}


}

class Salad {
private String greensType;
private String proteinType;
private ArrayList<String> toppings = new ArrayList<String>();

public Salad(String greensType) {
    this.greensType = greensType;
}

public String getGreensType() {
    return greensType;
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

public void addTopping(String topping) {
    toppings.add(topping);
}

}

```


---
## Example implementation of the OrderingSystem and Salad classes in Java:

---
## The Salad class has three private instance variables representing the salad's name, dressing, and calorie count. It has a constructor to initialize these variables, as well as getter methods to access them. It also overrides the toString() method to provide a string representation of the salad.The OrderingSystem class has a main method that prompts the user to enter information about salads they want to order. It creates Salad objects based on the user's input, adds them to a list of orders, and asks the user if they want to order another salad. Once the user is done ordering, it displays the list of orders to the user
---
```java
//JAVA
// OrderingSystem class
import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;

// Salad class
public class Salad {
    private String name;
    private String dressing;
    private int calories;

    public Salad(String name, String dressing, int calories) {
        this.name = name;
        this.dressing = dressing;
        this.calories = calories;
    }

    public String getName() {
        return name;
    }

    public String getDressing() {
        return dressing;
    }

    public int getCalories() {
        return calories;
    }

    @Override
    public String toString() {
        return name + " (Dressing: " + dressing + ", Calories: " + calories + ")";
    }
}

public class OrderingSystem {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        List<Salad> orders = new ArrayList<>();
        boolean keepOrdering = true;

        while (keepOrdering) {
            System.out.println("Please enter the salad name:");
            String name = scanner.nextLine();

            System.out.println("Please enter the dressing:");
            String dressing = scanner.nextLine();

            System.out.println("Please enter the calories:");
            int calories = scanner.nextInt();
            scanner.nextLine(); // consume the new line character

            Salad salad = new Salad(name, dressing, calories);
            orders.add(salad);

            System.out.println("Would you like to order another salad? (Y/N)");
            String answer = scanner.nextLine().toUpperCase();
            keepOrdering = answer.equals("Y");
        }

        System.out.println("Your orders are:");
        for (Salad salad : orders) {
            System.out.println(salad);
        }
    }
}


//JAVA

```

---

```java
/JAVA
import java.io.FileWriter;
import java.io.IOException;
import java.util.ArrayList;
import java.util.Scanner;
public class Salad {
    private String greensType;
    private String proteinType;
    private ArrayList<String> toppings;
    private boolean isVegan;
    private String dressing;
    
    public Salad(String greensType) {
        this.greensType = greensType;
        this.toppings = new ArrayList<String>();
        this.isVegan = true;
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
        if (proteinType.equals("tuna") || proteinType.equals("chicken")) {
            isVegan = false;
        }
    }
    
    public ArrayList<String> getToppings() {
        return toppings;
    }
    
    public void addTopping(String topping) {
        toppings.add(topping);
        if (topping.equals("cheese") || topping.equals("bacon")) {
            isVegan = false;
        }
    }
    
    public boolean isVegan() {
        return isVegan;
    }
    
    public String getDressing() {
        return dressing;
    }
    
    public void setDressing(String dressing) {
        this.dressing = dressing;
    }
}

public class OrderingSystem {
    public static void main(String[] args) {
        String greeting = "Welcome to Salads to Go!";
        String slogan = "Build Your Own Salads, Your Way. Time to build a salad.";
        Boolean isVegan = null;
        
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
        
        System.out.println(greeting);
        System.out.println(slogan);
        
        displayOptions("Salad greens", greens);
        Scanner scanner = new Scanner(System.in);
        System.out.print("What type of salad greens do you want? ");
        String greensChoice = scanner.nextLine();
        Salad salad = new Salad(greensChoice


public class Salad {
    private String greensType;
    private String proteinType;
    private ArrayList<String> toppings;
    private String dressing;
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
        if (proteinType.equals("tuna") || proteinType.equals("chicken")) {
            isVegan = false;
        } else {
            isVegan = true;
        }
    }
    
    public ArrayList<String> getToppings() {
        return toppings;
    }
    
    public void addTopping(String topping) {
        toppings.add(topping);
        if (topping.equals("cheese") || topping.equals("bacon")) {
            isVegan = false;
        }
    }
    
    public String getDressing() {
        return dressing;
    }
    
    public void setDressing(String dressing) {
        this.dressing = dressing;
    }
    
    public boolean isVegan() {
        return isVegan;
    }
}

```
---
Java - 2/14/2023

```java
//Here's an implementation of the Salad class: 

public class Salad {
    private String greensType;
    private String proteinType;
    private ArrayList<String> toppings;
    private boolean isVegan;
    private String dressing;

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

    public void setVegan(boolean vegan) {
        isVegan = vegan;
    }

    public String getDressing() {
        return dressing;
    }

    public void setDressing(String dressing) {
        this.dressing = dressing;
    }
}
//-------------------------------------------------

import java.util.ArrayList;

public class Salad {
    private String greensType;
    private String proteinType;
    private ArrayList<String> toppings;
    private boolean isVegan;
    private String dressing;

    public Salad(String greensType, String proteinType) {
        this.greensType = greensType;
        this.proteinType = proteinType;
        this.toppings = new ArrayList<String>();
        this.isVegan = true;
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

    public String getDressing() {
        return dressing;
    }

    public void setDressing(String dressing) {
        this.dressing = dressing;
    }
}
//-------------------------------------------------
public class Salad {
    private String greensType;
    private String proteinType;
    private ArrayList<String> toppings;
    private boolean isVegan;
    private String dressing;

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

    public void addTopping(String topping) {
        toppings.add(topping);
    }

    public boolean isVegan() {
        return isVegan;
    }

    public void setVegan(boolean isVegan) {
        this.isVegan = isVegan;
    }

    public String getDressing() {
        return dressing;
    }

    public void setDressing(String dressing) {
        this.dressing = dressing;
    }
}

//-------------------------------------------------
import java.util.ArrayList;

public class Salad {
    private String greens;
    private String protein;
    private ArrayList<String> toppings;
    private String dressing;
    private boolean isVegan;

    public Salad(String greens, String protein) {
        this.greens = greens;
        this.protein = protein;
        this.toppings = new ArrayList<String>();
        this.isVegan = true;
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

    public ArrayList<String> getToppings() {
        return toppings;
    }

    public void addTopping(String topping) {
        this.toppings.add(topping);
    }

    public String getDressing() {
        return dressing;
    }

    public void setDressing(String dressing) {
        this.dressing = dressing;
    }

    public boolean isVegan() {
        return isVegan;
    }

    public void setIsVegan(boolean isVegan) {
        this.isVegan = isVegan;
    }
}

//-------------------------------------------------
import java.util.ArrayList;

public class Salad {
    private String greensType;
    private String proteinType;
    private ArrayList<String> toppings;
    private boolean isVegan;
    private String dressing;

    public Salad(String greensType, String proteinType) {
        this.greensType = greensType;
        this.proteinType = proteinType;
        this.toppings = new ArrayList<>();
        this.isVegan = determineIsVegan(proteinType);
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
        this.isVegan = determineIsVegan(proteinType);
    }

    public ArrayList<String> getToppings() {
        return toppings;
    }

    public void addTopping(String topping) {
        toppings.add(topping);
        this.isVegan = determineIsVegan(toppings);
    }

    public boolean isVegan() {
        return isVegan;
    }

    public String getDressing() {
        return dressing;
    }

    public void setDressing(String dressing) {
        this.dressing = dressing;
    }

    private boolean determineIsVegan(String proteinType) {
        return !proteinType.equals("tuna") && !proteinType.equals("chicken");
    }

    private boolean determineIsVegan(ArrayList<String> toppings) {
        for (String topping : toppings) {
            if (topping.equals("cheese") || topping.equals("bacon")) {
                return false;
            }
        }
        return true;
    }
}

//-------------------------------------------------
public class Salad {
    private String greensType;
    private String proteinType;
    private ArrayList<String> toppings;
    private boolean isVegan;
    private String dressing;

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

    public void addTopping(String topping) {
        this.toppings.add(topping);
    }

    public boolean isVegan() {
        return isVegan;
    }

    public void setIsVegan(boolean isVegan) {
        this.isVegan = isVegan;
    }

    public String getDressing() {
        return dressing;
    }

    public void setDressing(String dressing) {
        this.dressing = dressing;
    }
}

//-------------------------------------------------
public class Salad {
    private String greensType;
    private String proteinType;
    private ArrayList<String> toppings;
    private boolean isVegan;
    private String dressing;

    public Salad(String greensType) {
        this.greensType = greensType;
        toppings = new ArrayList<String>();
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

    public String getDressing() {
        return dressing;
    }

    public void setDressing(String dressing) {
        this.dressing = dressing;
    }
}

//-------------------------------------------------
import java.util.ArrayList;

public class Salad {
    private String greensType;
    private String proteinType;
    private ArrayList<String> toppings;
    private boolean isVegan;
    private String dressing;

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
        if (proteinType.equals("tuna") || proteinType.equals("chicken")) {
            isVegan = false;
        } else if (proteinType.equals("black beans")) {
            isVegan = true;
        }
    }

    public ArrayList<String> getToppings() {
        return toppings;
    }

    public void setToppings(ArrayList<String> toppings) {
        this.toppings = toppings;
        for (String topping : toppings) {
            if (topping.equals("cheese") || topping.equals("bacon")) {
                isVegan = false;
                break;
            } else {
                isVegan = true;
            }
        }
    }

    public boolean isVegan() {
        return isVegan;
    }

    public String getDressing() {
        return dressing;
    }

    public void setDressing(String dressing) {
        this.dressing = dressing;
    }
}

//-------------------------------------------------
import java.io.FileWriter;
import java.io.IOException;
import java.util.ArrayList;
import java.util.Scanner;

public class OrderingSystem {
    public static void main(String[] args) {
        String greeting = "Welcome to Salads to Go!";
        String slogan = "Build Your Own Salads, Your Way. Time to build a salad.";
        boolean isVegan = true;

        // Initialize the lists of greens, proteins, and toppings
        ArrayList<String> greens = new ArrayList<String>();
        greens.add("kale");
        greens.add("romaine lettuce");
        greens.add("iceberg lettuce");

        ArrayList<String> proteins = new ArrayList<String>();
        proteins.add("tuna");
        proteins.add("chicken");
        proteins.add("black beans");

        ArrayList<String> toppings = new ArrayList<String>();
        toppings.add("cheese");
        toppings.add("croutons");
        toppings.add("tomatoes");
        toppings.add("onions");
        toppings.add("bacon");
        toppings.add("olives");

        // Display the greeting and slogan to the customer
        System.out.println(greeting);
        System.out.println(slogan);

        // Display the greens types to the customer
        System.out.println("Greens types:");
        for (String green : greens) {
            System.out.println("- " + green);
        }

        // Prompt the customer to choose a type of salad greens
        Scanner scanner = new Scanner(System.in);
        System.out.println("What type of salad greens do you want?");
        String chosenGreens = scanner.nextLine();

        // Create a new salad object with the chosen greens
        Salad salad = new Salad(chosenGreens);

        // Display the proteins to the customer
        System.out.println("Proteins:");
        for (String protein : proteins) {
            System.out.println("- " + protein);
        }

        // Prompt the customer to choose a type of protein
        System.out.println("What type of protein

//-------------------------------------------------
//-------------------------------------------------
//-------------------------------------------------
//-------------------------------------------------
//-------------------------------------------------
//-------------------------------------------------
// And here's an implementation of the OrderingSystem class:

import java.util.ArrayList;
import java.util.Scanner;
import java.io.FileWriter;
import java.io.IOException;

public class OrderingSystem {
    public static void main(String[] args) {
        // Greeting and slogan
        String greeting = "Welcome to Salads to Go!";
        String slogan = "Build Your Own Salads, Your Way. Time to build a salad.";

        // Boolean to track if the salad is vegan or not
        boolean isVegan = true;

        // Lists of greens, proteins, and toppings
        ArrayList<String> greens = new ArrayList<String>();
        greens.add("kale");
        greens.add("romaine lettuce");
        greens.add("iceberg lettuce");

        ArrayList<String> proteins = new ArrayList<String>();
        proteins.add("tuna");
        proteins.add("chicken");
        proteins.add("black beans");

        ArrayList<String> toppings = new ArrayList<String>();
        toppings.add("cheese");
        toppings.add("croutons");
        toppings.add("tomatoes");
        toppings.add("onions");
        toppings.add("bacon");
        toppings.add("olives");

        // Display options to the customer
        System.out.println(greeting);
        System.out.println(slogan);
        System.out.println("Here are the available greens:");
        for (String green : greens) {
            System.out.println("- " + green);
        }

        // Prompt the customer to choose a type of greens
        Scanner scanner = new Scanner(System.in);
        System.out.print("What type of salad greens do you want? ");
        String greensType = scanner.nextLine();

        // Create a new salad object with the chosen greens
        Salad salad = new Salad(greensType);

        // Display options to the customer
        System.out.println("Here are the available proteins:");
        for (String protein : proteins) {
            System.out.println("- " + protein);
        }

        // Prompt the customer to choose a type of protein
        System.out.print("What type of protein do you want? ");
        String proteinType = scanner.nextLine();

        // Set the type of protein on the salad object
        salad.setProteinType(proteinType);

        // Check if the protein is vegan
        if (proteinType.equals("tuna") || proteinType.equals("chicken")) {
            isVegan = false;
        }

        // Loop to choose toppings
        ArrayList<String>

//-------------------------------------------------
import java.util.ArrayList;
import java.util.Scanner;
import java.io.*;

public class OrderingSystem {
    public static void main(String[] args) {
        String greeting = "Welcome to Salads to Go!";
        String slogan = "Build Your Own Salads, Your Way. Time to build a salad.";
        boolean isVegan = true;
        ArrayList<String> greensTypes = new ArrayList<String>();
        greensTypes.add("kale");
        greensTypes.add("romaine lettuce");
        greensTypes.add("iceberg lettuce");
        ArrayList<String> proteinTypes = new ArrayList<String>();
        proteinTypes.add("tuna");
        proteinTypes.add("chicken");
        proteinTypes.add("black beans");
        ArrayList<String> toppingTypes = new ArrayList<String>();
        toppingTypes.add("cheese");
        toppingTypes.add("croutons");
        toppingTypes.add("tomatoes");
        toppingTypes.add("onions");
        toppingTypes.add("bacon");
        toppingTypes.add("olives");

        Scanner scanner = new Scanner(System.in);

        // Display greeting and slogan
        System.out.println(greeting);
        System.out.println(slogan);

        // Display greens types and prompt for choice
        System.out.println("Greens types:");
        for (String greensType : greensTypes) {
            System.out.println("- " + greensType);
        }
        System.out.print("What type of salad greens do you want? ");
        String greensChoice = scanner.nextLine();

        // Create salad with chosen greens type
        Salad salad = new Salad(greensChoice, null);

        // Display protein types and prompt for choice
        System.out.println("Protein types:");
        for (String proteinType : proteinTypes) {
            System.out.println("- " + proteinType);
        }
        System.out.print("What type of protein do you want? ");
        String proteinChoice = scanner.nextLine();

        // Set protein type on salad and check if it's vegan
        salad.setProteinType(proteinChoice);
        if (proteinChoice.equals("tuna") || proteinChoice.equals("chicken")) {
            salad.setVegan(false);
            isVegan = false;
        } else {
            salad.setVegan(true);
        }

        // Prompt
//-------------------------------------------------
import java.util.ArrayList;
import java.util.Scanner;
import java.io.FileWriter;
import java.io.IOException;

public class OrderingSystem {
    public static void main(String[] args) {
        String greeting = "Welcome to Salads to Go!";
        String slogan = "Build Your Own Salads, Your Way. Time to build a salad.";

        Boolean isVegan = true;

        ArrayList<String> greensTypes = new ArrayList<String>();
        greensTypes.add("kale");
        greensTypes.add("romaine lettuce");
        greensTypes.add("iceberg lettuce");

        ArrayList<String> proteinTypes = new ArrayList<String>();
        proteinTypes.add("tuna");
        proteinTypes.add("chicken");
        proteinTypes.add("black beans");

        ArrayList<String> toppingTypes = new ArrayList<String>();
        toppingTypes.add("cheese");
        toppingTypes.add("croutons");
        toppingTypes.add("tomatoes");
        toppingTypes.add("onions");
        toppingTypes.add("bacon");
        toppingTypes.add("olives");

        System.out.println(greeting);
        System.out.println(slogan);

        // Display greens types to the customer
        System.out.println("Available greens types:");
        for (String greensType : greensTypes) {
            System.out.println("- " + greensType);
        }

        // Prompt the customer to choose a type of salad greens
        Scanner scanner = new Scanner(System.in);
        System.out.print("What type of salad greens do you want? ");
        String greensChoice = scanner.nextLine();

        // Create a new salad object with the type of greens the customer has chosen
        Salad salad = new Salad(greensChoice);

        // Display protein types to the customer
        System.out.println("Available protein types:");
        for (String proteinType : proteinTypes) {
            System.out.println("- " + proteinType);
        }

        // Prompt the customer to choose a type of protein
        System.out.print("What type of protein do you want? ");
        String proteinChoice = scanner.nextLine();

        // Set the type of protein that the customer chose on the salad object
        salad.setProteinType(proteinChoice);

        // Determine if the protein the customer chose is vegan
        if (proteinChoice.equals("tuna") || proteinChoice.equals("chicken")) {
            isVegan = false;
        }
        salad.setVegan(isVegan);

       

//-------------------------------------------------
import java.io.FileWriter;
import java.io.IOException;
import java.util.ArrayList;
import java.util.Scanner;

public class OrderingSystem {
    public static void main(String[] args) {
        String greeting = "Welcome to Salads to Go!";
        String slogan = "Build Your Own Salads, Your Way. Time to build a salad.";
        Boolean isVegan = true;

        ArrayList<String> greens = new ArrayList<String>();
        greens.add("kale");
        greens.add("romaine lettuce");
        greens.add("iceberg lettuce");

        ArrayList<String> proteins = new ArrayList<String>();
        proteins.add("tuna");
        proteins.add("chicken");
        proteins.add("black beans");

        ArrayList<String> toppings = new ArrayList<String>();
        toppings.add("cheese");
        toppings.add("croutons");
        toppings.add("tomatoes");
        toppings.add("onions");
        toppings.add("bacon");
        toppings.add("olives");

        System.out.println(greeting);
        System.out.println(slogan);

        System.out.println("Greens types:");
        for (String green : greens) {
            System.out.println(green);
        }

        Scanner scanner = new Scanner(System.in);
        System.out.println("What type of salad greens do you want?");
        String chosenGreens = scanner.nextLine();

        Salad salad = new Salad(chosenGreens, "");

        System.out.println("Protein types:");
        for (String protein : proteins) {
            System.out.println(protein);
        }

        System.out.println("What type of protein do you want?");
        String chosenProtein = scanner.nextLine();

        salad.setProtein(chosenProtein);

        if (chosenProtein.equals("tuna") || chosenProtein.equals("chicken")) {
            salad.setIsVegan(false);
        }

        while (true) {
            System.out.println("Topping types:");
            for (String topping : toppings) {
                System.out.println(topping);
            }

            System.out.println("What type of topping do you want? (Enter 'done' to finish)");
            String chosenTopping = scanner.nextLine();

            if (chosenTopping.equals("done")) {
                break;
            }

            salad.addTopping(chosenTopping);

            if (chosenTopping.equals("cheese") || chosenTopping.equals("bacon")) {

//-------------------------------------------------
import java.io.FileWriter;
import java.io.IOException;
import java.util.ArrayList;
import java.util.Scanner;

public class OrderingSystem {
    public static void main(String[] args) {
        String greeting = "Welcome to Salads to Go!";
        String slogan = "Build Your Own Salads, Your Way. Time to build a salad.";
        boolean isVegan = true;

        ArrayList<String> greensTypes = new ArrayList<>();
        greensTypes.add("kale");
        greensTypes.add("romaine lettuce");
        greensTypes.add("iceberg lettuce");

        ArrayList<String> proteinTypes = new ArrayList<>();
        proteinTypes.add("tuna");
        proteinTypes.add("chicken");
        proteinTypes.add("black beans");

        ArrayList<String> toppingTypes = new ArrayList<>();
        toppingTypes.add("cheese");
        toppingTypes.add("croutons");
        toppingTypes.add("tomatoes");
        toppingTypes.add("onions");
        toppingTypes.add("bacon");
        toppingTypes.add("olives");

        displayOptions("Greens Types", greensTypes);
        String greensChoice = promptForChoice("What type of salad greens do you want?", greensTypes);
        Salad salad = new Salad(greensChoice, null);

        displayOptions("Protein Types", proteinTypes);
        String proteinChoice = promptForChoice("What type of protein do you want?", proteinTypes);
        salad.setProteinType(proteinChoice);

        ArrayList<String> toppings = new ArrayList<>();
        boolean wantMoreToppings = true;
        while (wantMoreToppings) {
            displayOptions("Topping Types", toppingTypes);
            String toppingChoice = promptForChoice("What type of topping do you want? (Press Enter to stop)", toppingTypes);
            if

//-------------------------------------------------
import java.util.ArrayList;
import java.util.Scanner;
import java.io.FileWriter;
import java.io.IOException;

public class OrderingSystem {
    public static void main(String[] args) {
        String greeting = "Welcome to Salads to Go!";
        String slogan = "Build Your Own Salads, Your Way. Time to build a salad.";

        Boolean isVegan = null;

        ArrayList<String> greensTypes = new ArrayList<String>();
        greensTypes.add("kale");
        greensTypes.add("romaine lettuce");
        greensTypes.add("iceberg lettuce");

        ArrayList<String> proteinTypes = new ArrayList<String>();
        proteinTypes.add("tuna");
        proteinTypes.add("chicken");
        proteinTypes.add("black beans");

        ArrayList<String> toppingTypes = new ArrayList<String>();
        toppingTypes.add("cheese");
        toppingTypes.add("croutons");
        toppingTypes.add("tomatoes");
        toppingTypes.add("onions");
        toppingTypes.add("bacon");
        toppingTypes.add("olives");

        System.out.println(greeting);
        System.out.println(slogan);

        System.out.println("Greens types:");
        for (String greensType : greensTypes) {
            System.out.println(greensType);
        }

        Scanner scanner = new Scanner(System.in);

        System.out.println("What type of salad greens do you want?");
        String greensType = scanner.nextLine();

        Salad salad = new Salad(greensType);

        System.out.println("Protein types:");
        for (String proteinType : proteinTypes) {
            System.out.println(proteinType);
        }

        System.out.println("What type of protein do you want?");
        String proteinType = scanner.nextLine();

        salad.setProteinType(proteinType);

        if (proteinType.equals("tuna") || proteinType.equals("chicken")) {
            isVegan = false;
        } else if (proteinType.equals("black beans")) {
            isVegan = true;
        }

        ArrayList<String> toppings = new ArrayList<String>();
        String topping = "";

        while (!topping.equals("done")) {
            System.out.println("What type of topping do you want? (Type 'done' if finished)");
            for (String toppingType : toppingTypes) {
                System.out.println(toppingType);
            }
            topping = scanner.nextLine();

            if (!topping

//-------------------------------------------------
import java.io.FileWriter;
import java.io.IOException;
import java.io.PrintWriter;
import java.util.ArrayList;
import java.util.Scanner;

public class OrderingSystem {
    public static void main(String[] args) {
        String greeting = "Welcome to Salads to Go!";
        String slogan = "Build Your Own Salads, Your Way. Time to build a salad.";
        Boolean isVegan = true;
        ArrayList<String> greensTypes = new ArrayList<String>();
        greensTypes.add("kale");
        greensTypes.add("romaine lettuce");
        greensTypes.add("iceberg lettuce");
        ArrayList<String> proteinTypes = new ArrayList<String>();
        proteinTypes.add("tuna");
        proteinTypes.add("chicken");
        proteinTypes.add("black beans");
        ArrayList<String> toppingTypes = new ArrayList<String>();
        toppingTypes.add("cheese");
        toppingTypes.add("croutons");
        toppingTypes.add("tomatoes");
        toppingTypes.add("onions");
        toppingTypes.add("bacon");
        toppingTypes.add("olives");

        // Display the greeting and the slogan to the customer
        System.out.println(greeting);
        System.out.println(slogan);

        // Display the greens types to the customer
        System.out.println("Choose your greens type:");
        for (String greensType : greensTypes) {
            System.out.println(greensType);
        }

        // Prompt the customer to choose a type of salad greens
        Scanner scanner = new Scanner(System.in);
        String chosenGreensType = scanner.nextLine();

        // Create a new salad object with the type of greens the customer has chosen
        Salad salad = new Salad(chosenGreensType);

        // Display the proteins to the customer
        System.out.println("Choose your protein type:");
        for (String proteinType : proteinTypes) {
            System.out.println(proteinType);
        }

        // Prompt the customer to choose a type of protein
        String chosenProteinType = scanner.nextLine();

        // Set the type of protein that the customer chose on the salad object
        salad.setProteinType(chosenProteinType);

        // Determine if the protein the customer chose is vegan
        if (chosenProteinType.equals("tuna") || chosenProteinType.equals("chicken")) {
            isVegan = false;
        }

        // Create a new empty ArrayList

//-------------------------------------------------
//-------------------------------------------------
//-------------------------------------------------
//-------------------------------------------------
//-------------------------------------------------
//-------------------------------------------------
//-------------------------------------------------
```

---
