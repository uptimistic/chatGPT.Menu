# chatGPT.Menu
## Experiment with chatGPT to generate Java code for a fast-food restaurant menu 
---

Here is an example Java program for a fast food menu:
---

---
---
Java - 2/14/2023
---
* Two java classes –an OrderingSystem class with a main method and a Salad class that will serve as a blueprint to create a new salad for the customer. 
* Create your Salad class. Add attributes to hold the type of greens, the type of protein, and the toppings the customer specifies. Add an attribute called isVegan to track if the salad is vegan or not. Add a constructor and the accessor methods (getters and setters.) 
* Create an Ordering system class with a main method. Add the code for the remaining requirements to the main method. 
* Declare a variable to hold the STG greeting: “Welcome to Salads to Go!” 
* Declare a variable to hold the STG slogan: “Build Your Own Salads, Your Way. Time to build a salad.” 
* Declare a Boolean variable called “isVegan”. (We will use this variable to track whether the user’s salad order is vegan or not.) 
*  Declare three ArrayLists to hold the types of greens, types of proteins, and types of toppings. Populate the lists with the values below. a. Greens types: kale, romaine lettuce, iceberg lettuce b. Proteins: tuna, chicken, or black beans c. Toppings: cheese, croutons, tomatoes, onions, bacon, and olives 
* Add a method to the application that displays the greens types, proteins, and toppings to the customer. Within the method, use a loop to iterate over the items in the list and display them to the customer. 
* Display the greeting and the slogan to the customer. 
* Call the method to display the greens types to the customer. 
* Then prompt the customer to choose a type of salad greens by asking “What type of salad greens do you want?” 
*  Create a new salad object and with the type of greens the customer has chosen. 
* Call the method to display the proteins to the customer. 
* Prompt the customer to choose a type of protein by asking “What type of protein do you want?” 
* Set the type of protein that the customer chose on the salad object. 
* Use a decision statement to determine if the proteinthe customer chose is vegan. Tuna and chicken are not vegan. The black beans are vegan.
* If the proteinis not vegan, set the isVegan property of the salad to false. If the proteinis vegan, set the isVegan property of the salad to true.
* Create a new empty ArrayList called “toppings”. This list will hold the toppings for the salad that are chosen by the customer. 
* Use a loop to keep prompting the customer to select another topping until the customer indicates they do not want any more toppings. 
    *  Inside the loop body, prompt the customer to choose a topping by asking “What type of topping do you want?” Then call the method to display the topping types to the customer. 
    * Inside the loop body, add the topping to the toppings list. 
    * Inside the loop body, use a decision statement to determine if the topping the customer chose is vegan. Cheese and baconare not vegan. Croutons, tomatoes, olives, and onions are vegan. If the topping is not vegan, set the isVegan property of the salad to false. If the topping is vegan, set the isVegan property of the salad to true. 
* Add the list of toppings to the salad object. 
* Display a message to the customer that says, “You ordered a [proteintype] salad on[greens type]. Use string concatenation to fill in the greens type and proteintype that the customer chose. 
* If the user chose at least one topping, display a message that says “Your salad is topped with: “. Then loop through the toppings on the salad and display them. 
* If the user ordered a vegan salad, display a message saying, “Thank you for trying our vegan salad.” Otherwise, display a message thanking the customer for ordering a salad from Salads to Go. 
* Open a file called SaladOrder.txt and write the information about the salad to the file, including the greens type, protein type, and toppings. 
* Add exception handling to catch any file I/O exceptions. 
* Refactor the Salad class so that it contains an attribute for dressing. 
* Then refactor your main method so the customer is prompted to choose a type of dressing and set the dressing value on your Salad object. 
*  display the dressing to the user and write it to the file with the rest of the order

---


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

public class Salad {
    private String greensType;
    private String proteinType;
    private ArrayList<String> toppings;
    private boolean isVegan;
    private String dressing;

    public Salad(String greensType) {
        this.greensType = greensType;
        this.toppings = new ArrayList<>();
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

    public void setToppings(ArrayList<String> toppings) {
        this.toppings = toppings;
        for (String topping : toppings) {
            if (topping.equals("cheese") || topping.equals("bacon")) {
                isVegan = false;
                break;
            }
            isVegan = true;
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
public class Salad {
    private String greens;
    private String protein;
    private ArrayList<String> toppings;
    private boolean isVegan;
    private String dressing;

    public Salad(String greens, String protein) {
        this.greens = greens;
        this.protein = protein;
        this.toppings = new ArrayList<>();
        this.isVegan = true;
    }

    public String getGreens() {
        return greens;
    }

    public String getProtein() {
        return protein;
    }

    public ArrayList<String> getToppings() {
        return toppings;
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

    public void addTopping(String topping) {
        toppings.add(topping);
        if (topping.equalsIgnoreCase("cheese") || topping.equalsIgnoreCase("bacon")) {
            isVegan = false;
        }
    }
}

//-------------------------------------------------
import java.util.ArrayList;

public class Salad {
    private String greensType;
    private String proteinType;
    private ArrayList<String> toppings;
    private String dressing;
    private boolean isVegan;

    public Salad(String greensType) {
        this.greensType = greensType;
        this.toppings = new ArrayList<>();
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

    public String getDressing() {
        return dressing;
    }

    public void setDressing(String dressing) {
        this.dressing = dressing;
    }

    public boolean isVegan() {
        return isVegan;
    }

    public void setVegan(boolean vegan) {
        isVegan = vegan;
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
        if (proteinType.equals("tuna") || proteinType.equals("chicken")) {
            this.isVegan = false;
        } else {
            this.isVegan = true;
        }
    }
    
    public ArrayList<String> getToppings() {
        return toppings;
    }
    
    public void setToppings(ArrayList<String> toppings) {
        this.toppings = toppings;
        for (String topping : toppings) {
            if (topping.equals("cheese") || topping.equals("bacon")) {
                this.isVegan = false;
                break;
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
    
    public String toString() {
        String result = "You ordered a " + proteinType + " salad on " + greensType;
        if (toppings.size() > 0) {
            result += " with the following toppings: " + String.join(", ", toppings);
        }
        result += ".\n";
        if (isVegan) {
            result += "Thank you for trying our vegan salad.";
        } else {
            result += "Thank you for ordering a salad from Salads to Go.";
        }
        return result;
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

    public String getDressing() {
        return dressing;
    }

    public void setDressing(String dressing) {
        this.dressing = dressing;
    }
}

//-------------------------------------------------
public class Salad {
    private String greens;
    private String protein;
    private ArrayList<String> toppings;
    private String dressing;
    private boolean isVegan;

    public Salad(String greens) {
        this.greens = greens;
        toppings = new ArrayList<>();
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
        if (protein.equals("tuna") || protein.equals("chicken")) {
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

//-------------------------------------------------
public class Salad {
    private String greens;
    private String protein;
    private ArrayList<String> toppings;
    private boolean isVegan;
    private String dressing;

    public Salad(String greens) {
        this.greens = greens;
        this.toppings = new ArrayList<>();
    }

    public String getGreens() {
        return greens;
    }

    public String getProtein() {
        return protein;
    }

    public void setProtein(String protein) {
        this.protein = protein;
        if (protein.equals("tuna") || protein.equals("chicken")) {
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
        isVegan = true;
    }

    public String getGreensType() {
        return greensType;
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

//-------------------------------------------------
public class Salad {
    private String greensType;
    private String proteinType;
    private boolean isVegan;
    private ArrayList<String> toppings;
    private String dressing;

    public Salad(String greensType) {
        this.greensType = greensType;
        this.toppings = new ArrayList<String>();
    }

    public String getGreensType() {
        return this.greensType;
    }

    public void setGreensType(String greensType) {
        this.greensType = greensType;
    }

    public String getProteinType() {
        return this.proteinType;
    }

    public void setProteinType(String proteinType) {
        this.proteinType = proteinType;
        if (proteinType.equals("tuna") || proteinType.equals("chicken")) {
            this.isVegan = false;
        } else {
            this.isVegan = true;
        }
    }

    public boolean isVegan() {
        return this.isVegan;
    }

    public ArrayList<String> getToppings() {
        return this.toppings;
    }

    public void addTopping(String topping) {
        this.toppings.add(topping);
        if (topping.equals("cheese") || topping.equals("bacon")) {
            this.isVegan = false;
        } else {
            this.isVegan = true;
        }
    }

    public String getDressing() {
        return this.dressing;
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
        this.isVegan = true; // Assume vegan until non-vegan topping is added
        this.dressing = "";
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
        toppings = new ArrayList<>();
        isVegan = true;
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

//-------------------------------------------------
//-------------------------------------------------
//-------------------------------------------------
//-------------------------------------------------
//-------------------------------------------------

// And here's an implementation of the OrderingSystem class:


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
import java.io.File;
import java.io.FileWriter;
import java.io.IOException;
import java.util.ArrayList;
import java.util.Scanner;

public class OrderingSystem {
    public static void main(String[] args) {
        String greeting = "Welcome to Salads to Go!";
        String slogan = "Build Your Own Salads, Your Way. Time to build a salad.";
        boolean isVegan;
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
        System.out.println(greeting);
        System.out.println(slogan);
        System.out.println("Here are the available greens types:");
        for (String greensType : greensTypes) {
            System.out.println(greensType);
        }
        System.out.print("What type of salad greens do you want? ");
        String greensType = scanner.nextLine();
        Salad salad = new Salad(greens
//-------------------------------------------------
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
import java.io.FileWriter;
import java.io.IOException;
import java.util.ArrayList;
import java.util.Scanner;

public class OrderingSystem {
    public static void main(String[] args) {
        // Greeting and slogan
        String greeting = "Welcome to Salads to Go!";
        String slogan = "Build Your Own Salads, Your Way. Time to build a salad.";

        // Greens types, protein types, and toppings
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

        // Display options to customer
        System.out.println(greeting);
        System.out.println(slogan);
        System.out.println("Greens types: ");
        for (String greensType : greensTypes) {
            System.out.println(greensType);
        }

        // Choose greens type
        Scanner scanner = new Scanner(System.in);
        System.out.println("What type of salad greens do you want?");
        String chosenGreensType = scanner.nextLine();
        Salad salad = new Salad(chosenGreensType);

        // Choose protein type
        System.out.println("Protein types: ");
        for (String proteinType : proteinTypes) {
            System.out.println(proteinType);
        }
        System.out.println("What type of protein do you want?");
        String chosenProteinType = scanner.nextLine();
        salad.setProteinType(chosenProteinType);

        // Choose toppings
        ArrayList<String> chosenToppings = new ArrayList<>();
        while (true) {

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

        displayMenu(greensTypes, proteins, toppings);

        Scanner scanner = new Scanner(System.in);

        System.out.println(greeting);
        System.out.println(slogan);

        System.out.println("What type of salad greens do you want?");
        String greensChoice = scanner.nextLine();
        Salad salad = new Salad(greensChoice, "");

        System.out.println("What type of protein do you want? (tuna, chicken, or black beans)");
        String proteinChoice = scanner.nextLine();
        salad.setProtein(proteinChoice);

        if (proteinChoice.equalsIgnoreCase("tuna") || proteinChoice.equalsIgnoreCase("chicken")) {
            isVegan = false;
        }

        ArrayList<String> selectedToppings = new ArrayList<>();
        String toppingChoice = "";

        while (!toppingChoice.equalsIgnoreCase("done")) {
            System.out.println("What type of topping do you want? (Type 'done' to finish)");
            toppingChoice = scanner.nextLine();
            if (toppingChoice.equalsIgnoreCase("done")) {
                break;
            }
            salad.addTopping(toppingChoice);
            selectedToppings.add(toppingChoice);
        }

        System.out.println("What type of dressing do you want?");
        String dressingChoice = scanner.nextLine();
        salad.setDressing(dressingChoice);

        System.out.println("You ordered a " + salad.getProtein() + " salad on " + salad.getGreens() + ".");

        if (!selectedToppings.isEmpty()) {
            System.out.print("Your salad is topped with: ");
            for (int i = 0; i < selectedT

//-------------------------------------------------
import java.io.FileWriter;
import java.io.IOException;
import java.util.ArrayList;
import java.util.Scanner;

public class OrderingSystem {
    public static void main(String[] args) {
        String greeting = "Welcome to Salads to Go!";
        String slogan = "Build Your Own Salads, Your Way. Time to build a salad.";

        // Declare the types of greens, proteins, and toppings
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

        Scanner scanner = new Scanner(System.in);

        // Display greeting and slogan
        System.out.println(greeting);
        System.out.println(slogan);

        // Display greens types
        System.out.println("Greens types:");
        for (String greensType : greensTypes) {
            System.out.println("- " + greensType);
        }

        // Prompt customer to choose greens type
        System.out.println("What type of salad greens do you want?");
        String greensType = scanner.nextLine();

        // Create new salad object with chosen greens type
        Salad salad = new Salad(greensType);

        // Display protein types
        System.out.println("Protein types:");
        for (String proteinType : proteinTypes) {
            System.out.println("- " + proteinType);
        }

        // Prompt customer to choose protein type
        System.out.println("What type of protein do you want?");
        String proteinType = scanner.nextLine();

        // Set protein type on salad object
        salad.setProteinType(proteinType);

        // Determine if protein type is vegan
        if (proteinType.equals("tuna") || proteinType.equals("chicken")) {
            salad.setVegan(false);
        } else {
            salad.setVegan(true);
        }

        // Prompt customer to choose toppings
        ArrayList<String> toppings = new ArrayList<>();
       
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

        // Display greens types
        System.out.println("Greens types:");
        for (String greensType : greensTypes) {
            System.out.println("- " + greensType);
        }

        // Prompt customer to choose greens type
        System.out.println("What type of salad greens do you want?");
        String greensTypeChoice = scanner.nextLine();

        // Create new salad object with chosen greens type
        Salad salad = new Salad(greensTypeChoice);

        // Display protein types
        System.out.println("Protein types:");
        for (String proteinType : proteinTypes) {
            System.out.println("- " + proteinType);
        }

        // Prompt customer to choose protein type
        System.out.println("What type of protein do you want?");
        String proteinTypeChoice = scanner.nextLine();

        // Set protein type on salad object
        salad.setProteinType(proteinTypeChoice);

        // Loop to

//-------------------------------------------------
    import java.io.BufferedWriter;
import java.io.FileWriter;
import java.io.IOException;
import java.util.ArrayList;
import java.util.Scanner;

public class OrderingSystem {
    public static void main(String[] args) {
        String greeting = "Welcome to Salads to Go!";
        String slogan = "Build Your Own Salads, Your Way. Time to build a salad.";
        System.out.println(greeting);
        System.out.println(slogan);

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

        System.out.println("Salad greens types:");
        for (String greensType : greensTypes) {
            System.out.println(greensType);
        }

        Scanner scanner = new Scanner(System.in);
        System.out.print("What type of salad greens do you want? ");
        String greensChoice = scanner.nextLine();
        Salad salad = new Salad(greensChoice);

        System.out.println("Protein types:");
        for (String proteinType : proteinTypes) {
            System.out.println(proteinType);
        }

        System.out.print("What type of protein do you want? ");
        String proteinChoice = scanner.nextLine();
        salad.setProtein(proteinChoice);

        ArrayList<String> toppings = new ArrayList<>();
        boolean wantMoreToppings = true;
        while (wantMoreToppings) {
            System.out.println("Topping types:");
            for (String toppingType : toppingTypes) {
                System.out.println(toppingType);
            }

            System.out.print("What type of topping do you want? ");
            String toppingChoice = scanner.nextLine();
            salad.addTopping(toppingChoice);

            System.out.print("Do you want more toppings? (yes/no) ");
            String moreToppingsChoice = scanner.nextLine();
            if (

//-------------------------------------------------
    import java.io.BufferedWriter;
import java.io.FileWriter;
import java.io.IOException;
import java.util.ArrayList;
import java.util.Scanner;

public class OrderingSystem {
    public static void main(String[] args) {
        String greeting = "Welcome to Salads to Go!";
        String slogan = "Build Your Own Salads, Your Way. Time to build a salad.";
        boolean isVegan = true;
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

        Scanner scanner = new Scanner(System.in);
        System.out.println(greeting);
        System.out.println(slogan);

        // Display greens types
        System.out.println("Choose your greens:");
        for (String green : greens) {
            System.out.println("- " + green);
        }

        // Prompt for greens type
        System.out.print("What type of salad greens do you want? ");
        String greensType = scanner.nextLine();

        // Create new salad object with chosen greens type
        Salad salad = new Salad(greensType);

        // Display protein types
        System.out.println("Choose your protein:");
        for (String protein : proteins) {
            System.out.println("- " + protein);
        }

        // Prompt for protein type
        System.out.print("What type of protein do you want? ");
        String proteinType = scanner.nextLine();

        // Set protein type on salad object
        salad.setProtein(proteinType);

        // Prompt for toppings
        ArrayList<String> chosenToppings = new ArrayList<>();
        while (true) {
            // Display topping types
            System.out.println("Choose your toppings (enter 'done' when finished):");
            for (String topping : toppings) {
                System.out.println("- " + topping);
            }

            // Prompt for topping

//-------------------------------------------------
import java.io.FileWriter;
import java.io.IOException;
import java.util.ArrayList;
import java.util.Scanner;

public class OrderingSystem {
    public static void main(String[] args) {
        String greeting = "Welcome to Salads to Go!";
        String slogan = "Build Your Own Salads, Your Way. Time to build a salad.";
        System.out.println(greeting);
        System.out.println(slogan);

        // Create the greens, protein, and topping ArrayLists
        ArrayList<String> greens = new ArrayList<>();
        greens.add("kale");
        greens.add("romaine lettuce");
        greens.add("iceberg lettuce");

        ArrayList<String> protein = new ArrayList<>();
        protein.add("tuna");
        protein.add("chicken");
        protein.add("black beans");

        ArrayList<String> toppings = new ArrayList<>();
        toppings.add("cheese");
        toppings.add("croutons");
        toppings.add("tomatoes");
        toppings.add("onions");
        toppings.add("bacon");
        toppings.add("olives");

        // Display the greens types, proteins, and toppings to the customer
        displayList("Greens types", greens);
        displayList("Proteins", protein);
        displayList("Toppings", toppings);

        // Prompt the customer to choose a type of salad greens
        Scanner scanner = new Scanner(System.in);
        System.out.println("What type of salad greens do you want?");
        String chosenGreens = scanner.nextLine();

        // Create a new salad object with the chosen greens
        Salad salad = new Salad(chosenGreens);

        // Prompt the customer to choose a type of protein
        System.out.println("What type of protein do you want?");
        String chosenProtein = scanner.nextLine();

        // Set the type of protein that the customer chose on the salad object
        salad.setProtein(chosenProtein);

        // Determine if the protein is vegan or not
        boolean isVegan = true;
        if (chosenProtein.equals("tuna") || chosenProtein.equals("chicken")) {
            isVegan = false;
        }
        salad.setIsVegan(isVegan);

        // Prompt the customer to select toppings
        System.out.println("What type of topping do you want? Type 'done' to finish.");
        String chosenTopping = scanner.nextLine();
        while (!chosenTopping.equals("done")) {
            // Add the topping to the toppings list
            toppings.add(chosenTopping);

            // Determine if the topping is vegan or not
            if (chosenTopping.equals("cheese") || chosenTopping.equals("bacon")) {
                isVegan = false;
            }
            salad.setIsVegan(isVegan);

            // Prompt the customer to select another topping
            System.out.println("What type of topping do you want? Type 'done' to finish.");
            chosenTopping = scanner.nextLine();
        }

        // Add the list of toppings to the salad object
        salad.setToppings(toppings);

        // Display the salad order to the customer
        System.out.println("You ordered a " + chosenProtein + " salad on " + chosenGreens + ".");
        if (!toppings.isEmpty()) {
            System.out.print("Your salad is topped with: ");
            for (String topping : toppings) {
                System.out.print(topping + " ");
            }
            System.out.println();
        }

        if (isVegan) {
            System.out.println("Thank you for trying our vegan salad.");
        } else {
            System.out.println("Thank you for ordering a salad from Salads to Go.");
        }

        // Prompt the

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

        displayItems("Greens types:", greensTypes);
        Scanner scanner = new Scanner(System.in);
        System.out.print("What type of salad greens do you want? ");
        String greensChoice = scanner.nextLine();

        Salad salad = new Salad(greensChoice);

        displayItems("Protein types:", proteinTypes);
        System.out.print("What type of protein do you want? ");
        String proteinChoice = scanner.nextLine();
        salad.setProteinType(proteinChoice);

        ArrayList<String> toppings = new ArrayList<String>();
        boolean keepAddingToppings = true;
        while (keepAddingToppings) {
            displayItems("Topping types:", toppingTypes);
            System.out.print("What type of topping do you want? (type 'done' to finish) ");
            String toppingChoice = scanner.nextLine();
            if (toppingChoice.equals("done")) {
                keepAddingToppings = false;
            } else {
                salad.addTopping(toppingChoice);
            }
        }

        System.out.println("You ordered a " + salad.getProteinType() + " salad on " + salad.getGreensType() + ".");
        ArrayList<String> saladToppings = salad.getToppings();
        if (saladToppings.size() > 0) {
            System

//-------------------------------------------------
import java.io.BufferedWriter;
import java.io.FileWriter;
import java.io.IOException;
import java.util.ArrayList;
import java.util.Scanner;

public class OrderingSystem {
    public static void main(String[] args) {
        // Declare variables
        String greeting = "Welcome to Salads to Go!";
        String slogan = "Build Your Own Salads, Your Way. Time to build a salad.";
        boolean isVegan;
        ArrayList<String> greensTypes = new ArrayList<String>();
        ArrayList<String> proteinTypes = new ArrayList<String>();
        ArrayList<String> toppingTypes = new ArrayList<String>();
        ArrayList<String> toppings = new ArrayList<String>();

        // Populate lists
        greensTypes.add("kale");
        greensTypes.add("romaine lettuce");
        greensTypes.add("iceberg lettuce");

        proteinTypes.add("tuna");
        proteinTypes.add("chicken");
        proteinTypes.add("black beans");

        toppingTypes.add("cheese");
        toppingTypes.add("croutons");
        toppingTypes.add("tomatoes");
        toppingTypes.add("onions");
        toppingTypes.add("bacon");
        toppingTypes.add("olives");

        // Display greens, proteins, and toppings
        displayItems("Greens types:", greensTypes);
        displayItems("Protein types:", proteinTypes);
        displayItems("Topping types:", toppingTypes);

        // Prompt user to choose greens
        Scanner scanner = new Scanner(System.in);
        System.out.print("What type of salad greens do you want? ");
        String greensType = scanner.nextLine();
        Salad salad = new Salad(greensType);

        // Prompt user to choose protein
        System.out.print("What type of protein do you want? ");
        String proteinType = scanner.nextLine();
        salad.setProteinType(proteinType);

        // Prompt user to choose toppings
        while (true) {
            System.out.print("What type of topping do you want? (Enter \"done\" to finish) ");
            String topping = scanner.nextLine

//-------------------------------------------------
import java.util.ArrayList;
import java.util.Scanner;
import java.io.FileWriter;
import java.io.IOException;

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

        displayOptions("Greens types", greensTypes);
        Scanner scanner = new Scanner(System.in);
        System.out.print("What type of salad greens do you want? ");
        String greensChoice = scanner.nextLine();
        Salad salad = new Salad(greensChoice);
        System.out.println();
        
        displayOptions("Protein types", proteinTypes);
        System.out.print("What type of protein do you want? ");
        String proteinChoice = scanner.nextLine();
        salad.setProteinType(proteinChoice);
        System.out.println();
        
        ArrayList<String> chosenToppings = new ArrayList<String>();
        String toppingChoice = "";
        while (!toppingChoice.equals("none")) {
            displayOptions("Topping types", toppingTypes);
            System.out.print("What type of topping do you want? (Enter 'none' to stop selecting toppings) ");
            toppingChoice = scanner.nextLine();
            if (!toppingChoice.equals("none")) {
                salad.addTopping(toppingChoice);
                chosenToppings.add(toppingChoice);
            }

//-------------------------------------------------
import java.io.FileWriter;
import java.io.IOException;
import java.util.ArrayList;
import java.util.Scanner;

public class OrderingSystem {
    public static void main(String[] args) {
        // Greeting and slogan
        String greeting = "Welcome to Salads to Go!";
        String slogan = "Build Your Own Salads, Your Way. Time to build a salad.";

        // List of greens, proteins, and toppings
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

        // Display menu to customer
        System.out.println(greeting);
        System.out.println(slogan);

        System.out.println("Greens:");
        for (String green : greens) {
            System.out.println(green);
        }

        System.out.println("Proteins:");
        for (String protein : proteins) {
            System.out.println(protein);
        }

        System.out.println("Toppings:");
        for (String topping : toppings) {
            System.out.println(topping);
        }

        // Prompt for greens and protein
        Scanner scanner = new Scanner(System.in);

        System.out.println("What type of salad greens do you want?");
        String greensType = scanner.nextLine();

        System.out.println("What type of protein do you want?");
        String proteinType = scanner.nextLine();

        // Create new salad object
        Salad salad = new Salad(greensType, proteinType);

        // Prompt for toppings
        ArrayList<String> chosenToppings = new ArrayList<>();
        while (true) {
            System.out.println("What type of topping do you want? (Type 'done' to finish)");
            String chosenTopping = scanner.nextLine();
            if (chosenTopping.equalsIgnoreCase("done")) {
                break;
            }
            chosenToppings.add(chosenTopping);

            //

//-------------------------------------------------
import java.io.BufferedWriter;
import java.io.FileWriter;
import java.io.IOException;
import java.util.ArrayList;
import java.util.Scanner;

public class OrderingSystem {
    private static final String GREETING = "Welcome to Salads to Go!";
    private static final String SLOGAN = "Build Your Own Salads, Your Way. Time to build a salad.";

    private static final ArrayList<String> GREENS_TYPES = new ArrayList<>(
            ArrayList.of("kale", "romaine lettuce", "iceberg lettuce"));
    private static final ArrayList<String> PROTEIN_TYPES = new ArrayList<>(ArrayList.of("tuna", "chicken", "black beans"));
    private static final ArrayList<String> TOPPING_TYPES = new ArrayList<>(
            ArrayList.of("cheese", "croutons", "tomatoes", "onions", "bacon", "olives"));

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Salad salad = createSalad(scanner);

        displayGreetingAndSlogan();
        displayGreensTypes();
        String greensType = promptForGreensType(scanner);
        salad.setGreensType(greensType);

        displayProteinTypes();
        String proteinType = promptForProteinType(scanner);
        salad.setProteinType(proteinType);
        if (proteinType.equals("tuna") || proteinType.equals("chicken")) {
            salad.setIsVegan(false);
        }

        ArrayList<String> toppings = chooseToppings(scanner);
        salad.setToppings(toppings);

        displaySaladInformation(salad);
        writeOrderToFile(salad);
    }

    private static Salad createSalad(Scanner scanner) {
        System.out.println("Let's create a new salad!");

        displayGreensTypes();
        String greensType = promptForGreensType(scanner);

        displayProteinTypes();
        String proteinType = promptForProteinType(scanner);

        return new Salad(greensType, proteinType);
    }

    private static void displayGreetingAndSlogan() {
        System.out.println(GREETING);

//-------------------------------------------------
import java.io.BufferedWriter;
import java.io.FileWriter;
import java.io.IOException;
import java.util.ArrayList;
import java.util.Scanner;

public class OrderingSystem {
    public static void main(String[] args) {
        String greeting = "Welcome to Salads to Go!";
        String slogan = "Build Your Own Salads, Your Way. Time to build a salad.";
        boolean isVegan;
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

        displayOptions(greensTypes, "salad greens");
        String greensChoice = promptChoice("What type of salad greens do you want?");
        Salad salad = new Salad(greensChoice);

        displayOptions(proteinTypes, "protein");
        String proteinChoice = promptChoice("What type of protein do you want?");
        salad.setProteinType(proteinChoice);

        ArrayList<String> toppings = new ArrayList<>();
        String toppingChoice;
        do {
            displayOptions(toppingTypes, "topping");
            toppingChoice = promptChoice("What type of topping do you want? (press Enter to finish)");
            if (!toppingChoice.isEmpty()) {
                toppings.add(toppingChoice);
                salad.addTopping(toppingChoice);
            }
        } while (!toppingChoice.isEmpty());

        displaySaladDetails(salad);

        if (salad.getToppings().size() > 0) {
            System.out.print("Your salad is topped with: ");
            for (String topping : salad.getToppings()) {
                System.out.print(topping + ", ");
            }

//-------------------------------------------------
//-------------------------------------------------
//-------------------------------------------------
//-------------------------------------------------
//-------------------------------------------------
    
```
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
