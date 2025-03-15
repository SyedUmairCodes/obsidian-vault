# Nested Conditionals

Nested conditionals are `if` statements (or `if-else` statements) placed *inside* other `if` or `else` blocks.  This allows you to create more complex decision-making logic in your code.  It's like a decision tree: the first `if` statement is the root, and each nested `if` creates a new branch based on the outcome of the previous condition.

They handle situations where one decision depends on the outcome of a previous decision.  The video's initial example of choosing a morning drink (coffee or tea, then black coffee or with milk, or tea with lemon) is a perfect illustration.  The choice of milk only matters *if* you've already chosen coffee.

```java
if (condition1) {
// Code to execute if condition1 is true
	if (condition2) {
	// Code to execute if condition1 AND condition2 are true
	}
	else {
		// Code to execute if condition1 is true, but condition2 is false
        }
    } else {
        // Code to execute if condition1 is false
        if (condition3) {
          //Code to execute if condition1 is false AND condition3 is true
        }
    }
```

You can nest `if` statements within `if` blocks, within `else` blocks, or have a mix of both.  The key is that the inner `if` statement is only evaluated if the outer condition is met.

## Related Notes