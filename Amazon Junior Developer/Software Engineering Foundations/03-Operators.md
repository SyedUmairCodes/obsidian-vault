# Operators in Java

Java has arithmetic, relational, and logical operators.  Arithmetic operators do math.  Relational operators compare values.  Logical operators combine conditions.

**Arithmetic Operators:**
*   `+` (addition)
*   `-` (subtraction)
*   `*` (multiplication)
*   `/` (division) - Be careful with integer division!  `7 / 2` results in `3`, not `3.5`.  To get `3.5`, at least one of the operands needs to be a `double`.
*   `%` (modulo) - Gives the remainder of a division.  `7 % 2` results in `1`.
*   `++` (increment) - Increases the value by 1.  Can be prefix (`++x`) or postfix (`x++`).  The difference matters in expressions.
*   `--` (decrement) - Decreases the value by 1.  Also has prefix and postfix forms.

**Relational Operators:**
*   `==` (equal to) - *Don't* confuse this with `=`, which is the assignment operator.
*   `!=` (not equal to)
*   `>` (greater than)
*   `<` (less than)
*   `>=` (greater than or equal to)
*   `<=` (less than or equal to)

**Logical Operators:**
*   `&&` (logical AND) - Both sides must be `true` for the result to be `true`.
*   `||` (logical OR) - At least one side must be `true` for the result to be `true`.
*   `!` (logical NOT) - Inverts the boolean value.

> The `+` operator, when used with at least one `String`, performs concatenation (joining strings together).

Just like in math, operators have a specific order of precedence.  For example, multiplication and division are performed before addition and subtraction.  Use parentheses `()` to override the default precedence and make your code clearer.

**Short-Circuit Evaluation (for `&&` and `||`):** 
*   With `&&`, if the left side is `false`, the right side is *not* evaluated because the overall result will be `false` anyway.
*   With `||`, if the left side is `true`, the right side is *not* evaluated because the overall result will be `true` anyway.

```java
public class OperatorExamples {
	public static void main(String[] args) {
	// Arithmetic operators
		int x = 10;
		int y = 3;
		System.out.println("x + y = " + (x + y)); // 13
		System.out.println("x - y = " + (x - y)); // 7
		System.out.println("x * y = " + (x * y)); // 30
		System.out.println("x / y = " + (x / y)); // 3 (integer division)
		System.out.println("x % y = " + (x % y)); // 1
		System.out.println("x / (double)y = " + (x / (double)y)); //3.3333

	// Relational operators
		System.out.println("x == y: " + (x == y)); // false
		System.out.println("x != y: " + (x != y)); // true
		System.out.println("x > y: " + (x > y));  // true
		System.out.println("x < y: " + (x < y));  // false

	// Logical operators
		boolean a = true;
		boolean b = false;
		System.out.println("a && b: " + (a && b)); // false
		System.out.println("a || b: " + (a || b)); // true
		System.out.println("!a: " + (!a));       // false

	// String concatenation
		String firstName = "John";
		String lastName = "Doe";
		System.out.println("Full name: " + firstName + " " + lastName); // John Doe

	// Increment/Decrement
		int count = 5;
		System.out.println("count++: " + (count++)); // Prints 5, then increments to 6
		System.out.println("count: " + count);       // Prints 6
		System.out.println("++count: " + (++count)); // Increments to 7, then prints 7

	//Short circuit
		int num = 5;
		if (num > 10 && num++ < 20 ) {
			System.out.println("This won't print");}
            System.out.println(num); //Prints 5
        }
    }
    ```

## Related Notes