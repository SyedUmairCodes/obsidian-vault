# Iterating Loops

Loops allow you to execute a block of code repeatedly, either a fixed number of times (like sending emails to a known list) or until a certain condition is met (like keeping asking a user for input until they provide valid data).

## The `for` Loop

The `for` loop is ideal when you know *in advance* how many times you want to repeat a block of code.  It's often used for counting or iterating over a known sequence.

```java
    for (initialization; condition; change) {
        // Code to be repeated
    }
```

*   **`initialization`:** This part is executed *once* at the beginning of the loop. It's typically used to declare and initialize a *loop counter* variable (often named `i`, `j`, or `k`).  Example: `int i = 0;`
*   **`condition`:** This is a *boolean expression* that is checked *before each iteration* of the loop.  If the condition is `true`, the loop body is executed.  If it's `false`, the loop terminates.  Example: `i < 5;`
*   **`change`:** This part is executed *after each iteration* of the loop.  It's typically used to update the loop counter variable.  Example: `i++;` (increment `i` by 1) or `i--;` (decrement `i` by 1)
* You can use the increment operator (`++`) to count up, or the decrement operator (`--`) to count down.

## The `while` Loop

The `while` loop is used when you want to repeat a block of code *as long as a condition is true*, and you *don't necessarily know in advance* how many times the loop will run. A `For` loop has the initial value, condition, and change statement. A `While` loop only has the condition. The other parts are often, but not always, taken care of inside the while block.

```java
    while (condition) {
        // Code to be repeated
    }
```

*   **`condition`:**  A boolean expression.  The loop continues as long as this condition is `true`.  If the condition is *initially* `false`, the loop body is *never* executed.

>[!Danger]
> **Infinite Loops:** Be *very careful* to ensure that the condition in your `while` loop will *eventually* become `false`.  Otherwise, you'll create an *infinite loop*, and your program will never terminate.

## The `do-while` Loop

The `do-while` loop is similar to the `while` loop, but the key difference is that the code block is executed *at least once*, *before* the condition is checked.

```java
    do {
        // Code to be repeated (at least once)
    } while (condition);  // Note the semicolon!
```

*   The code inside the `do` block is executed *first*.
*   *Then*, the `condition` is checked.  If it's `true`, the loop repeats.  If it's `false`, the loop terminates.

## Examples: Number Guesser

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
      Scanner keyboard = new Scanner(System.in);
      // the secret number is 7
      int guess;
      do {
        System.out.print("Guess the number between 1 and 9");
        guess = keyboard.nextInt();
      } while(guess != 7); //repeat until number is 7

      System.out.println("Congrats you got it right!");
    }
}
```

## Related Notes