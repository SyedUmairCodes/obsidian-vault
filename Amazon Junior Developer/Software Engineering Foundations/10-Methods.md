# Methods in Java

Methods are blocks of code that perform a specific task. They are like mini-programs within your larger program.  Methods break down a large, complex problem into smaller, more manageable pieces.  This makes your code easier to understand, write, and debug.

Once you've defined a method, you can call (use) it multiple times from different parts of your program, without having to rewrite the same code.  Methods make your code more organized and easier to read.  Well-named methods act like comments, explaining what each part of your program does.

> If you need to change how a particular task is performed, you only need to modify the method, not every place in your code where that task is done.

```java
<access_modifier> <static_or_not> <return_type> <method_name>(<parameter_list>) {
    // Method body (the code that performs the task)
}

public static string returnName(){}
```

- Access modifiers control the visibility of the method.
- A static method belongs to the *class* itself, not to a specific *instance* (object) of the class. 
- The return type specifies the type of data the method returns.
- Name of the method that tell what the method does.
- Methods can accept parameters if required.

Non-Returning methods perform an action but don't return a value. Returning methods perform a calculation or retrieve some data and *return* a value to the caller.  The `return` type specifies what kind of value is returned.

```java
public static int add(int x, int y) {
	int sum = x + y;
	return sum; // Returns the value of sum (an int)
    }

//calling a method that returns an integer
int z = add(5,3);
```

## The Main Method

This is the special method that serves as the *entry point* for your Java program.  When you run a Java program, the Java Virtual Machine (JVM) looks for this method and starts executing your code from there. The method must be named main and it's parameters must include `String[] args`.

## Related Notes