# Polymorphism

In Object-Oriented Programming, polymorphism is a fundamental concept that allows objects of different classes to be treated as objects of a common superclass. 

More specifically, it's the ability of a single variable, method parameter, or collection item (like an element in a list) to refer to objects of different types (related by inheritance) and automatically invoke the *correct* method specific to the object's actual type at runtime.

You have a reference (like a remote control) that can point to different types of objects (like a TV, a Blu-ray player, a Soundbar), and when you press a button (call a method like `turnOn()`), the *specific* device it's pointing to performs *its own* version of that action.

Polymorphism relies heavily on inheritance. You have a superclass (e.g., `Vehicle`) and one or more subclasses (e.g., `Car`, `Motorcycle`) that `extend` the superclass. This establishes the "is-a" relationship (`Car` *is-a* `Vehicle`, `Motorcycle` *is-a* `Vehicle`).

> [!Note]
> The subclasses often provide their own specific implementations of methods inherited from the superclass. This is called **Method Overriding**. The method in the subclass must have the *exact same signature* (name, return type, and parameter list) as the method in the superclass.

When you call a method using the *superclass reference*, the Java Virtual Machine (JVM) determines *at runtime* (when the program is executing) which version of the method to run based on the **actual type of the object** the reference is currently pointing to, *not* the type of the reference variable itself.

## Related Notes

- [[16-Inheritance]]