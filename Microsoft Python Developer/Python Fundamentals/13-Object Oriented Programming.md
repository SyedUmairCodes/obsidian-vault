# Object Oriented Programming

- **Objects:** Represent real-world entities or abstract concepts. They have properties (attributes) and can perform actions (methods). Think of them as individual "things" in your program.
   
- **Classes:** Blueprints or templates for creating objects. They define the common attributes and methods that objects of a specific type will have. Think of a class as the general concept and objects as specific examples of that concept.
  
## Key Principles of OOP

- **Encapsulation:** Bundling data (attributes) and the methods that operate on that data within a class. This hides internal details and protects the object's state. Think of it like a capsule containing both medicine (data) and instructions (methods). Python uses a single underscore _ convention to indicate internal attributes.

- **Abstraction:** Simplifying complex systems by presenting only essential information to the user, hiding unnecessary implementation details. Think of it like the simple interface of your phone – you don't need to know how the internal circuits work to use it.

- **Inheritance:** Creating new classes (child classes or subclasses) based on existing ones (parent classes or superclasses), inheriting their attributes and methods. This promotes code reuse and establishes "is-a" relationships. For example, a Dog class inherits from an Animal class because a dog "is a" type of animal.

- **Polymorphism:** The ability of objects of different classes to respond to the same method call in their own way. This allows you to write more flexible and generic code. Think of a draw() method that works differently for a Circle object and a Square object.

```Python
class Dog:
    def __init__(self, name, breed):
        self.name = name
        self.breed = breed

    def bark(self):
        print(f"Woof! My name is {self.name} and I'm a {self.breed}.")


# Create a Dog object
my_dog = Dog("Buddy", "Golden Retriever")

# Call the bark method
my_dog.bark() # Output: Woof! My name is Buddy and I'm a Golden Retriever.
```