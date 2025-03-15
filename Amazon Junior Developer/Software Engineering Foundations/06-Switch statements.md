# Switch Statements

When you need to check if a variable is equal to one of several *specific* values, a `switch` statement is often a cleaner and more efficient way to do it than using a long chain of `if-else if-else` statements.

An ice cream shop offering different flavors on different days.  This is a good way to visualize how a `switch` statement works:

*   **The Variable:**  Think of the variable being checked as the "day of the week" (or, in the later example, the user's desired ice cream flavor).
*   **The Cases:**  Each `case` within the `switch` statement represents a specific value that the variable might have (e.g., "Monday," "Tuesday," or "Strawberry," "Vanilla").
*   **The Code Blocks:** The code inside each `case` block is what happens if the variable matches that particular value (e.g., "Today's special is Chocolate Chip Cookie Dough!").
* **The Default.** The default case is what happens when the variable is not equal to any of the specified cases.

```java
switch (variableWhoseValueIsComparedToCaseValue) {  // Variable to be checked
    case value1:
        // Code to execute if variable == value1
        break; // IMPORTANT!
    case value2:
        // Code to execute if variable == value2
        break;
    case value3:
        // Code to execute if variable == value3
        break;
    default:
        // Code to execute if variable doesn't match any of the cases
}
```

*   **Switch (variable):**  The `switch` keyword starts the statement.  The `variable` inside the parentheses is the variable whose value will be checked.  
*   **Case value::**  Each `case` label specifies a *constant* value.  If the `variable` is *equal* to this `value`, the code following the colon (`:`) will be executed.  
*   **Break:** The `break` statement is *crucial*.  It exits the `switch` statement.  If you *omit* the `break`, execution will "fall through" to the next `case`, even if that `case` doesn't match. 
*   **Default:** The `default` case is optional.  It's like the final `else` in an `if-else if` chain.  If none of the `case` values match the `variable`, the code inside the `default` block is executed.

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner keyboard = new Scanner(System.in);

        System.out.println("Enter the flavor you want:");
        String iceCreamFlavour = keyboard.nextLine();

        switch (iceCreamFlavour) {
            case "Strawberry":
                System.out.println("I will enjoy my Strawberry ice cream.");
                break; // Essential to prevent fallthrough
            case "Vanilla":
                System.out.println("I will enjoy my Vanilla ice cream.");
                break;
            case "Mango":
                System.out.println("I will enjoy my Mango ice cream.");
                break;
            case "Chocolate":
                System.out.println("I will enjoy my Chocolate ice cream.");
                break;
            default:
                System.out.println("I will have a glass of cold water.");
        }
    }
}
```

## Calculator Example

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner keyboard = new Scanner(System.in);

        System.out.print("Enter the first number: ");
        double number1 = keyboard.nextDouble(); // Use double for more flexibility

	// "Burn" the newline after reading the double
        keyboard.nextLine();

        System.out.print("Enter the second number: ");
        double number2 = keyboard.nextDouble(); // Use double

	// "Burn" the newline again
        keyboard.nextLine();

        System.out.print("Enter the operator (+, -, *, /): ");
        String operator = keyboard.nextLine(); // Read the operator as a String

        double result = 0.0; // Initialize the result.  Use double.

        switch (operator) {
            case "+":
                result = number1 + number2;
                break;
            case "-":
                result = number1 - number2;
                break;
            case "*":
                result = number1 * number2;
                break;
            case "/":
		// Handle division by zero!  VERY IMPORTANT
                if (number2 != 0) {
                    result = number1 / number2;
                } else {
                    System.out.println("Error: Cannot divide by zero.");
		// You might want to exit the program or ask for input again here.
		// For simplicity, we'll just set the result to 0.
                    result = 0;
                }
                break;
            default:
                System.out.println("Invalid operator.");
        }

        System.out.println("The result is: " + result);

        keyboard.close(); // Good practice
    }
}
```

## Related Notes