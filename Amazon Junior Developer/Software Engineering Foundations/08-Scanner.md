# User Input with Scanner

The `Scanner` class (from the `java.util` package) allows you to read input from the user (typically from the keyboard).

*   You need to `import java.util.Scanner;` at the top of your file.
*   You create a `Scanner` object: `Scanner keyboard = new Scanner(System.in);`
*   You use methods like `nextInt()`, `nextDouble()`, `nextLine()`, etc., to read different data types.

```java
import java.util.Scanner; // Import the Scanner class

public class ScannerExample {
	public static void main(String[] args) {
		Scanner keyboard = new Scanner(System.in); // Create a Scanner object

		System.out.print("Enter your age: ");
		int age = keyboard.nextInt(); // Read an integer

		keyboard.nextLine(); // Consume the leftover newline

		System.out.print("Enter your name: ");
		String name = keyboard.nextLine(); // Read a line of text

		System.out.print("Enter your height (in meters): ");
		double height = keyboard.nextDouble(); // Read a double

		System.out.println("Hello, " + name + "!");
		System.out.println("You are " + age + " years old.");
		System.out.println("Your height is " + height + " meters.");

		keyboard.close(); // Close the Scanner (good practice)
        }
    }
```

## Related Notes