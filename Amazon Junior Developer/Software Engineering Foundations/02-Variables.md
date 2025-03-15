# Variables in Java

Variables are like containers that store data.  You declare them with a type and a name, and you can initialize them with a value.  Java has various data types like `int`, `double`, `char`, `String`, and `boolean`.  There are naming conventions (camelCase) to follow.
   
**Declaration vs. Initialization:** 
*   **Declaration:**  `int playerScore;`  
*   **Initialization:**  `playerScore = 150;`  

Java is *very* case-sensitive.  `playerScore`, `PlayerScore`, and `PLAYERSCORE` are all treated as *completely different* variables.

**Naming Conventions:**
*   **Variables:** `camelCase` (e.g., `playerScore`, `numberOfLives`)
*   **Classes:** `PascalCase` (also known as `UpperCamelCase`) (e.g., `PlayerScore`, `GameController`)
*   **Constants:** `UPPER_SNAKE_CASE` (e.g., `MAX_PLAYERS`, `PI`) 


    ```java
    public class VariableExamples {
        public static void main(String[] args) {
            // Declaration and initialization
            int age;
            age = 30;

            // Combined declaration and initialization
            double price = 19.99;

            // char (single quotes)
            char initial = 'J';

            // String (double quotes)
            String name = "Alice";

            // boolean
            boolean isGameOver = false;

            // Demonstrating case sensitivity
            int myVariable = 10;
            // int MyVariable = 20; // This would be a DIFFERENT variable

            // Printing variables
            System.out.println("Age: " + age);
            System.out.println("Price: " + price);
            System.out.println("Initial: " + initial);
            System.out.println("Name: " + name);
            System.out.println("Is game over? " + isGameOver);
            System.out.println("My Variable: " + myVariable);
        }
    }
    ```

## Related Notes