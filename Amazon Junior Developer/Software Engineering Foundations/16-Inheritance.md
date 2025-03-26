# Inheritance

Think about inheriting traits from your parents – eye color, maybe a particular way you laugh. In Object-Oriented Programming, **Inheritance** is a mechanism where a new class (the **subclass** or **child class**) derives properties (data) and methods (behaviors) from an existing class (the **superclass** or **parent class**).

>[!Note]
>It establishes an **"is-a" relationship**. If we have a `Car` class that inherits from a `Vehicle` class, we can say a `Car` *is-a* `Vehicle`.

Imagine you have a instruction booklet for a basic car (the `Vehicle` superclass). It tells you how to build the chassis, add wheels, and a steering mechanism and common properties and methods like `accelerate()`, `brake()`, `turn()`.

Now, you want to build a `FireTruck` or a `MonsterTruck` . Instead of starting from scratch, you use the basic car instructions and then add the specific parts: a ladder for the `FireTruck`, giant tires for the `MonsterTruck`.

## The SUPER Keyword
We know subclasses inherit methods and properties. Sometimes, a subclass needs to perform an action that is *based on* or *includes* the action defined in its superclass, possibly adding extra steps. This is where explicitly calling a superclass method becomes useful.

## Related Notes