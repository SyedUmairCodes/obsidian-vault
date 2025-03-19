# Method Arguments

Arguments (also called parameters) are values that you *pass into* a method when you call it.  They are the inputs that the method uses to do its work.  

Arguments make methods much more flexible and reusable.  Instead of writing a separate method for every possible input, you can write a *single* method that takes arguments and behaves differently based on the values of those arguments.

```java
    public static <return_type> <method_name>(<parameter_list>) {
        // Method body
    }
```

The `<parameter_list>` is where you define the arguments. Each argument has a *type* and a *name*:

```java
    public static int calculateDamage(int strength) { ... } // One argument: int strength

    public static double calculateArea(double length, double width) { ... } // Two arguments: double length, double width

    public static void printMessage(String message) { ... } //One argument: String message
    ```

```java
int damage = calculatePunchDamage(20);  // Call the method with strength = 20
System.out.println(damage); // Prints 40

double area = calculateArea(5.0, 10.0); // Call with length = 5.0, width = 10.0
```

```java
public static double calculateSpecialAttackDamage(int strength, String attackType) {
    int damage = strength;
    if (attackType.equals("fire punch")) {
        damage *= 3; // Multiply damage by 3
    } else if (attackType.equals("ice blast")) {
        damage *= 2; // Multiply damage by 2
    }
    return damage;
}
```

## Related Notes

- [[10-Methods]]