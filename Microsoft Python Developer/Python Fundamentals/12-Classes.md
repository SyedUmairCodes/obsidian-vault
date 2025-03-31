# Classes in Python

Think of a class as a blueprint or a template for creating objects. It's like a master plan that defines the common characteristics (attributes) and behaviors (methods) of a group of similar things.

- A car blueprint (the class) defines common features like the number of wheels, engine type, color options, etc. (attributes).
- It also defines what a car can do: accelerate, brake, turn, etc. (methods).

Each individual car built from the blueprint is an object (an instance of the car class). Each car might have different specific values for the attributes (e.g., red color, 4-cylinder engine), but they all share the same basic structure and capabilities defined by the class. In Python terms, you instantiate an object from a class.

## Key Abilities of Classes

- **Encapsulation:** Bundling data (attributes) and the functions that operate on that data (methods) together into a single unit (the class). This is like a toolbox - all the tools related to a specific task are organized in one container. This makes code more organized and easier to maintain.

- **Inheritance:** Creating new classes (child classes) based on existing classes (parent classes). The child class inherits all the attributes and methods of the parent and can add its own unique features or modify existing ones.

- **Polymorphism:** The ability of objects of different classes to respond to the same method call in their own way.

## Components of a Python Class

- **Attributes:** Variables that hold data about an object. (e.g., car.color = "red", car.engine = "V6") 
- **Methods:** Functions that define what an object can do. (e.g., car.accelerate(), car.brake())
- **Constructor (__init__)**: A special method that is automatically called when you create a new object. It is used to initialize the object's attributes. (e.g., setting the car's color and engine type when it's first created).

## Example

``` Python
class BankAccount:
    def __init__(self, account_holder, initial_balance): # Constructor
        self.account_holder = account_holder  # Attribute
        self.balance = initial_balance      # Attribute

    def deposit(self, amount):              # Method
        self.balance += amount

    def withdraw(self, amount):             # Method
        if amount <= self.balance:
            self.balance -= amount
        else:
            print("Insufficient funds!")


# Create an object (instantiate)
alice_account = BankAccount("Alice", 1000) # Alice's account with initial balance of 1000

# Use the object's methods
alice_account.deposit(500)
alice_account.withdraw(200)
print(alice_account.balance)  # Output: 1300


bob_account = BankAccount("Bob", 500) # Creating a different BankAccount object for bob
```

## Custom Classes

Custom classes provide a way to organize your code into logical, reusable units. They're like blueprints for creating objects, allowing you to group related data (attributes) and functions (methods) that operate on that data. This addresses the problems of large projects by:

- **Identify Key Concepts (Nouns):** Look for the main nouns or entities in your project description. These often represent good candidates for classes.
- **Define Attributes (Properties):** For each class, determine what data or properties are relevant to that concept. These become the class's attributes.
- **Define Methods (Behaviors):** Think about what actions or operations each object of the class should be able to perform. These become the class's methods.
### Example

``` Python
class Book:
    def __init__(self, title, author, isbn):
        self.title = title
        self.author = author
        self.isbn = isbn
        self.is_checked_out = False  

    def check_out(self):
        if not self.is_checked_out:
           self.is_checked_out = True
           print(f"{self.title} has been checked out.")
        else:
           print(f"{self.title} is already checked out.")

    def check_in(self):
       if self.is_checked_out:
           self.is_checked_out = False
           print(f"{self.title} has been checked in.")
       else:
           print(f"{self.title} is already checked in.")


# Create instances (objects) of the Book class
book1 = Book("The Lord of the Rings", "J.R.R. Tolkien", "978-0618079109")
book2 = Book("To Kill a Mockingbird", "Harper Lee", "978-0061120083")

# Interact with the objects
book1.check_out() # Output: The Lord of the Rings has been checked out.
book2.check_out() # Output: To Kill a Mockingbird has been checked out.
book1.check_in()  # Output: The Lord of the Rings has been checked in.
book1.check_in() # Output: The Lord of the Rings is already checked in.
```

---
