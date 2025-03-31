# Loops in Python

Loops (for and while) are crucial for handling repetitive tasks, enabling efficient processing of large datasets, complex calculations, and streamlined logic. This is especially important in data science, web development, and automation.

Loops reduce code duplication, leading to cleaner, more maintainable code. The lecture emphasizes that loops are fundamental to writing efficient and effective code.

**For Loops:** Designed for iterating over sequences with a known length (lists, tuples, strings, ranges).

```Python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
```

 **For i Loop:** Iterates over a sequence of numbers using the `range()` function. Commonly used when the exact number of iterations is known.

```Python
for i in range(5):  # Loops from 0 to 4
    print(i)
```

**For Each Loop:** Iterates over each element in a sequence directly. This is useful for processing each item in a list or other iterable. 

```Python
student_scores = {"Alice": 90, "Bob": 85, "Charlie": 88}
for name, score in student_scores.items():
    print(f"{name} scored {score}")
```

**While Loops:** Execute as long as a specified condition remains true. They are ideal when the number of iterations is unknown beforehand. 

```Python
x = 5
while x > 0:
    print(x)
    x -= 1  # Decrease x by 1
```

**Nested Loops:** Placing a loop inside another (nesting) enables processing multi-dimensional data or performing complex operations.

```Python
for i in range(3):
    for j in range(2):
        print(f"i={i}, j={j}")
```
## Related Notes