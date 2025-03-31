# Mutability
Mutability refers to the ability of an object (like a data structure) to be changed after it's created.  

* **Mutable:**  Objects can be modified after creation (e.g., adding, removing, or changing elements).
* **Immutable:** Objects *cannot* be modified after creation.  Any operation that seems to modify an immutable object actually creates a *new* object.
## Mutable Data Structures

* **Lists:**  Ordered collections of items.  Allow adding, removing, changing order, and modifying elements. 
* **Dictionaries:** Collections of key-value pairs.  Allow adding new pairs, modifying existing values, and removing pairs. 
## Why Mutability Matters
Modifying a mutable object in place is often faster than creating a new object every time a change is needed. If you pass a mutable object to a function and the function modifies it, the original object will also be changed.  This can be intentional but can also lead to unexpected bugs if not carefully managed.
## Immutable Data Structures

* **Tuples:** Ordered, unchangeable sequences.
* **Sets:** Unordered collections of unique elements (no duplicates).
## Benefits of Immutability

* **Predictability:**  Code behavior is easier to understand when data cannot change unexpectedly.
* **Optimization:** Python can potentially optimize immutable data structures for faster execution and lower memory usage.
* **Dictionary Keys:** Tuples can be used as dictionary keys because their immutability guarantees that the key won't change, ensuring consistent lookups.  (Some immutable sets - frozensets - can be keys as well.)
## Use cases

* **Mutable (Lists, Dictionaries):** Use when data needs to be modified frequently, for dynamic content, real-time updates, or data transformation. 
* **Immutable (Tuples, Sets):** Use when data integrity is paramount, when data should remain constant, or when a data structure is needed as a dictionary key.
