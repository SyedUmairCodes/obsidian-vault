# Data Types

A data type is fundamentally a combination of a *set of values* and a *set of operations* defined on those values. Java provides built-in primitive types(int, float, boolean, etc.).

While we *could* theoretically build everything using only these, it would be incredibly cumbersome and difficult to manage for complex problems. Primitives lack the expressive power needed to model real-world entities or complex data structures effectively. This limitation motivates data abstraction. Just as function abstraction allows us to use a function without knowing its internal workings, data abstraction lets us work with higher-level concepts.

Java empowers data abstraction primarily through reference types, implemented using the `class` construct. This is the cornerstone of Object-Oriented Programming (OOP). Instead of just manipulating raw numbers, we create objects – instances of classes, which hold data (state) and provide operations (methods) to interact with that data.

>[!Note]
>You are not limited to predefined classes. Java allows you to define your *own* data types by writing your own classes, enabling you to model *any* entity or concept relevant to the problem you're solving.

## Abstract Data Types

An Abstract Data Type (ADT)is a *mathematical model* or a *specification* for a data type. It defines:

*   What data it *conceptually* represents.
*   What operations it supports (its **API** - Application Programming Interface).

When you *use* an ADT, you interact with it *only* through its defined API (its public methods). You focus on *what* it does, not *how* it does it. When you *implement* an ADT, you write a concrete Java class. Here, you *do* care about the internal data representation (the instance variables) and how to code the methods defined in the API to manipulate that data correctly and efficiently.

The Java Development Kit (JDK) itself provides thousands of built-in ADTs. Every non-trivial Java class you write effectively defines a new data type, often intended to function as an ADT (even if simple).

- Core System ADTs  are fundamental to the Java language and are automatically available in every program without needing an `import` statement. 
- Standard Library ADTs provide vast libraries packed with ADTs for various tasks – collections, input/output, networking, graphics, and much more. To use these, you typically need an `import` statement (e.g., `import java.util.ArrayList;`). 
- Custom  ADTs are ADTs we define ourselves within our projects for our required usecase.

## Encapsulation

The principle of encapsulation is a cornerstone of Object-Oriented Programming and the key to unlocking numerous benefits in software design. By enforcing this separation between the *what* (the API) and the *how* (the implementation), encapsulation enables true modular programming.

- Client code and ADT implementation code can be developed, tested, and debugged largely in isolation. The API serves as the clear, stable interface between them.
- Bugs or changes within an ADT's implementation are contained. As long as the API contract is upheld, fixes or internal modifications won't break client code.
- A well-defined ADT becomes a reusable component, effectively extending the language itself. 
- We can develop a *new, improved implementation* of an ADT – perhaps one using a more efficient underlying data structure or algorithm – and substitute it for the old one. 
- Encapsulation allows the implementer to add internal consistency checks, debugging aids, and assertions without cluttering the client's view.

> [!Note]
> The client trusts the API contract; the implementer fulfills it. This mutual agreement, this disciplined ignorance of internal details, is what makes modularity and substitutability possible.

Designing good APIs is one of the *most important, yet most challenging*, tasks in modern software development. This isn't an afterthought; it's a core activity that requires practice, careful deliberation, and often, multiple iterations to get right.

The effort is crucial because, as your notes point out, time invested upfront in crafting a clear, usable API is invariably repaid downstream. A well-designed API leads to:

- Clear contracts make it easier to pinpoint whether errors lie in the client code or the ADT implementation.
- A good API makes the component inviting and understandable for future use, potentially by different developers or in different projects.
- It reinforces the separation of concerns we've been discussing.

You should adopt the mindset that *any* code you write might need to be reused someday. Thinking in terms of clear APIs, even for smaller components, cultivates good design habits.


## Related Notes

- [[16-Inheritance]]