# Lists in Python

Python lists can store elements of different data types (numbers, strings, booleans, other lists), making them highly adaptable. This is contrasted with arrays in some languages that have type restrictions.

> [!Note]
> Lists can be modified after creation (adding, removing, changing elements and maintain the order in which elements are added. 

```Python
new_list = [] #empty list
even_list = [2,4,6,8] #pre-filled list
```

- `print(even_list)` displays the list's contents within square brackets, separated by commas. Elements in a list are accessed by their index (position), starting from 0.
- `len(even_list)` returns the number of elements in the list.
- Extracting a portion of the list using `even_list[0:2]`. 
- Adding new elements to the end of a list using `append()`.
- `IndexError` (accessing an invalid index) and `ValueError` (using a list method incorrectly). 
- Two-Dimensional Lists: Lists within lists, creating a grid-like structure. 

> [!Note]
> For loops are particularly well-suited for traversing lists, processing each element one by one.

## Related Notes