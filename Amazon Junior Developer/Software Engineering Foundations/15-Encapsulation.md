# Encapsulation

Encapsulation is one of the core principles of OOP. It means **bundling** an object's data (its properties or state) and the methods (its behaviors or actions) that operate on that data into a single unit – the class.

>Crucially, it also involves **controlling access** to that data and methods, selectively hiding the internal complexity and exposing only what's necessary.

Just like you don't need to know the phone's internal workings, you don't need to learn about the internal workings of the built-in methods. You just need to know *how to call it*. It also helps in protecting the integrity of the data by not allowing any accidental or malicious modification that could lead to invalid states.

If the internal implementation of a method needs to change, you can modify the code *inside* the method. As long as the way you *call* the method (its signature) remains the same, other parts of the program that use it won't break.

Declare the class properties (instance variables) as `private`. The `private` keyword means these properties can *only* be accessed directly from *within* the curly braces `{}` of the class itself.

```java
    public class Robot {
        private int batteryCharge; // Hidden from outside
        // ... other properties and methods
    }
    ```

To allow controlled reading and writing of private properties from outside the class, we use special public methods:

**Getter:** A method that retrieves the value of a private property. By convention, it starts with `get` followed by the property name. It returns a value of the same type as the property.
**Setter:** A method that modifies the value of a private property. By convention, it starts with `set` followed by the property name. It takes a parameter of the same type as the property and usually returns `void`. 

## Access Control

Encapsulation relies heavily on controlling *who* can access *what*. This control is achieved using **Access Modifiers**. 

- Public members (class, property, method) are accessible from *anywhere* – within its own class, from other classes in the same package, from subclasses (even in different packages), and from any code outside the package.
- Private members are accessible *only* from *within* the defining class itself. No other class, not even a subclass.
- Protected members are accessible from within the defining class itself, subclasses, and any other class in the same package.   

> [!Note] 
> If you don't specify any access modifier (`public`, `private`, or `protected`), the member has `default` access. It is accessible only from within its own class and by other classes in the *same package*. It's *not* accessible to subclasses in *different* packages.
 
| Modifier    | Same Class | Same Package | Subclass (Same Pkg) | Subclass (Diff Pkg) | Global (Diff Pkg) |
| :---------- | :--------: | :----------: | :-----------------: | :-----------------: | :---------------: |
| `public`    |    Yes     |     Yes      |         Yes         |         Yes         |        Yes        |
| `protected` |    Yes     |     Yes      |         Yes         |         Yes         |        No         |
| `default`   |    Yes     |     Yes      |         Yes         |         No          |        No         |
| `private`   |    Yes     |      No      |         No          |         No          |        No         |

## Related Notes