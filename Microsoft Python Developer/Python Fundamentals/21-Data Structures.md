# Data Structures

Just like you use containers (bags, baskets) to organize groceries, Python uses data structures to organize data.  This makes data easier to store, access, and manipulate.

* **Lists (Ordered Collections):**  Think of a numbered grocery list.  Lists maintain the order of items.  You can access items by their position (index), add items, remove items, and modify existing items. 
* **Dictionaries (Key-Value Pairs):** Imagine each item having a price tag. Dictionaries store information in key-value pairs. You can quickly look up a value (price) using its associated key (item name). Dictionaries are great for representing relationships between data. 
* **Sets (Unique Elements):** Like a collection of unique spices. Sets only store unique elements; duplicates are automatically removed. This is useful for checking if an item already exists or for finding common elements between collections. 

## Lists
Ordered, mutable (changeable) sequences of items. Can contain mixed data types.

```Python
my_list = [1, 2, "hello", [3, 4]]
```

- **Indexing:** Access elements by position (starts from 0). my_list[0] (gets the first element)
- **Slicing:** Extract a portion of the list. my_list[1:3] (gets the second and third elements)
- **append():** Add an item to the end.
- **insert():** Add an item at a specific position.
- **remove():** Remove an item by value.
- **pop():** Remove and return an item by position.
- **extend():** Add multiple items from another list. my_list.extend([5,6])
- **sort():** Sort the list in place.
- **reverse():** Reverse the order of elements.
## Tuples
Ordered, immutable (unchangeable) sequences of items. Can contain mixed data types. Immutability provides data integrity.
```Python
my_tuple = (10, 20, "python")
```

- **Key Operations:** Similar indexing and slicing as lists, but no methods to add, remove, or modify elements.
- **Use Case Example:** Geographic coordinates, storing data that should not be changed.
## Sets
Unordered collections of unique items. No duplicates allowed.

```Python
my_set = {1, 2, 3, 3} (duplicates are automatically removed)
```

- **add():** Add an element.
- **remove():** Remove an element.
- **union():** Combine elements from two sets.
- **intersection():** Find common elements.
- **difference():** Find elements in one set but not the other.
## Dictionaries
Collections of key-value pairs. Keys must be unique and immutable (often strings or numbers). Values can be any data type.

```Python
my_dict = {"name": "Alice", "age": 30, "city": "New York"}
```

- **Accessing Values:** my_dict["name"] (returns "Alice")
- **get():** Safely retrieve a value, returns None if key doesn't exist. my_dict.get("country", "Unknown")
- **items():** Get all key-value pairs.
- **keys():** Get all keys.
- **values():** Get all values.
- **update():** Merge another dictionary.


