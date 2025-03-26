# Interfaces

An interface is like a 100% abstract class. It defines a "contract" of what methods a class *must* implement if it agrees to adhere to that interface. It specifies *what* a class should be able to do, but not *how* it does it. You define one using the `interface` keyword instead of `class`.

```java
    public interface Cookable {
        // Method signatures only - no implementation (no curly braces {})
        void prepareIngredients();
        void cookMeal();
        void cleanup();
    }
```

All methods declared in an interface (prior to Java 8 default methods) are implicitly `public` and `abstract`. You just provide the method signature followed by a semicolon `;`. There's no method body and any variables (fields) declared in an interface are implicitly `public`, `static`, and `final`. They are constants and must be initialized when declared.

```java
public interface Drivable {
	int MAX_SPEED_MPH = 120; // public static final implicitly
	void startEngine();
	void accelerate(int targetSpeed);
	void steer(String direction);
	void brake();
}
```

A class doesn't extend an interface; it implements it. This signifies that the class agrees to fulfill the contract defined by the interface. It must provide a concrete implementation for every abstract method declared in the interface(s) it implements.

> A class can implement *multiple* interfaces, separated by commas. This is how Java achieves a form of "multiple inheritance" – inheriting multiple *contracts* or *types*.


>[!Note]
>If a class declares implements an Interface but fails to provide an implementation for *even one* abstract method from that interface, the compiler will give an error *unless* the class itself is declared abstract. An abstract class doesn't have to implement all interface methods immediately.

## Related Notes