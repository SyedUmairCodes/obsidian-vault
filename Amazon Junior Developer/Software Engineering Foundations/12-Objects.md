# Objects in Java

An object is a specific *instance* of a class (like `fireFist` or `frostBlizzard`).  You create objects using the `new` keyword.  Each object has its *own* set of data (state).

Every object in Java has a unique memory address. When you declare a variable of a class type (e.g., `Hero fireFist;`), you're creating a *reference variable*. This variable doesn't hold the object itself; it holds the *memory address* (the reference) of the object.

```java
    public class Hero {
        // Member variables (state)
        String name;
        int strength;
        int health;

        // ... methods ...
    }
```

 Each `Hero` object will have its *own* `name`, `strength`, and `health`.  Changing the `strength` of one `Hero` object doesn't affect the `strength` of any other `Hero` object.

## Related Notes