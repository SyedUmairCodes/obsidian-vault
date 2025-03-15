# Conditional Statements

Conditional statements allow your program to make decisions based on whether a condition is true or false.

* `if` statements execute a block of code if a condition is true.
* `else` statements provide an alternative block of code to execute if the `if` condition is false.
* `else if` statements allow you to check multiple conditions in sequence.  Only the block of code associated with the *first* true condition is executed.
* The final `else` in an `if-else if` chain is optional and acts as a "catch-all" if none of the previous conditions are true.

> The "condition" in an `if` statement (or `else if`) is a *boolean expression*.  This means it's an expression that evaluates to either `true` or `false`.


*   **Nested `if`:**  Used when a decision *depends* on the outcome of a previous decision.  The inner `if` is only checked if the outer `if` is true.
*   **`else if`:**  Used when you have a series of *mutually exclusive* conditions.  You want to check them in order, and only execute the block for the *first* one that's true.

```java
public class ConditionalExamples {
	public static void main(String[] args) {
		int age = 25;
		int money = 150;

	// Simple if statement
		if (age >= 18) {
			System.out.println("You are an adult."); }

	// if-else statement
		if (money >= 200) {
			System.out.println("You can afford a nice dinner.");}
		 else {
			System.out.println("You might want to choose a cheaper option."); }

	// if-else if chain
		if (age < 13) {
			System.out.println("You are a child."); } 
		else if (age < 18) {
			System.out.println("You are a teenager.");}
		else if (age < 65) {
			System.out.println("You are an adult.");} 
		else {
			System.out.println("You are a senior citizen.");}
        }
    }
```

## Related Notes
