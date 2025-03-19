# Constructors

We create objects and then *separately* set their attributes using the dot operator.

```java
Car colorado = new Car();
colorado.make = "Chevrolet";
colorado.model = "Colorado";
colorado.color = "Red";

Car mustang = new Car();
mustang.make = "Ford";
mustang.model = "Mustang";
mustang.color = "Blue";
```

This works, but it has some drawbacks:

*   **Tedious:**  It's repetitive to set each attribute individually.
*   **Error-Prone:** You might forget to set an attribute, leaving the object in an incomplete or inconsistent state.
*   **Not Encapsulated:** The object's internal state is directly exposed and manipulated from outside the class.  This violates the principle of *encapsulation*, a core OOP concept.

Constructors are special methods that are *automatically* called when you create a new object using the `new` keyword. Their primary purpose is to *initialize* the object's state (set the initial values of its member variables).

 **Key Characteristics of Constructors:**
*   **Same Name as the Class:**  A constructor *must* have the same name as the class it belongs to.
*   **No Return Type:**  Constructors *do not* have a return type, not even `void`. This is a key difference from regular methods.
*   **Automatically Called:** You don't call constructors directly (like you do with regular methods).  They are invoked automatically when you use `new`.
*   **Purpose: Initialization:** The primary job of a constructor is to set up the object's initial state.

## Types of Constructors


- **Default Constructor:** If you *don't* define *any* constructors in your class, Java automatically provides a *default constructor*.
 
```java
    public class Car {
        String make;
        String model;
        String color;
    }
    // somewhere else
    Car myCar = new Car(); // The default constructor is called
    System.out.println(myCar.make); // Prints null
    ```

*   **No-Argument Constructor:** This is a constructor that you *explicitly* define, and it takes *no arguments*.

```java
    public class Car {
        String make;
        String model;
        String color;

        // No-argument constructor
        public Car() {
            this.make = "Unknown";
            this.model = "Unknown";
            this.color = "Unknown";
        }
    }

    // somewhere else
    Car myCar = new Car(); // Calls the no-arg constructor
    System.out.println(myCar.make); // Prints "Unknown"
    ```

*   **Parameterized Constructor:** This is a constructor that *takes arguments*.  You use these arguments to initialize the object's attributes with *specific values* provided *at the time of object creation*.

```java
    public class Car {
        String make;
        String model;
        String color;

        // Parameterized constructor
        public Car(String make, String model, String color) {
            this.make = make;
            this.model = model;
            this.color = color;
        }
    }

    // somewhere else
    Car myCar = new Car("Toyota", "Camry", "Silver"); // Calls the parameterized constructor
    System.out.println(myCar.make); // Prints "Toyota"
    ```

 You can have *multiple* constructors in a class, as long as they have *different parameter lists* (different numbers, types, or order of parameters). This is called *constructor overloading*. It's a form of *method overloading*.

```java
    public class Car {
        String make;
        String model;
        String color;

        // No-argument constructor
        public Car() {
            this.make = "Unknown";
            this.model = "Unknown";
            this.color = "Unknown";
        }

        // Parameterized constructor (all attributes)
        public Car(String make, String model, String color) {
            this.make = make;
            this.model = model;
            this.color = color;
        }

        // Parameterized constructor (only make and model)
        public Car(String make, String model) {
            this.make = make;
            this.model = model;
            this.color = "Unknown"; // Default color
        }
    }
    //
    Car car1 = new Car(); // Uses the no-arg constructor
    Car car2 = new Car("Honda", "Civic", "Blue"); // Uses the 3-arg constructor
    Car car3 = new Car("Tesla", "Model 3"); // Uses the 2-arg constructor
    ```

## Related Notes