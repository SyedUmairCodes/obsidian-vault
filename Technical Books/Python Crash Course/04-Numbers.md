# Numeric Values in Python

Almost all kind of programming requires working with numbers. Be it single or multi-digit integers or floating-points, calculations cannot be done without them. The four basic arithmetic operations are done easily in Python using the + sign for addition, - for subtraction, \* for multiplication, and / for division.

Python supports the order of operations as well if you are calculating multiple values in a single statement. The order can be changed based on how you would like to calculate the result.

```Python
2+3*4 # Will return 14
(2+3)*4 # will return 20
```

## Floating points
Any numeric value that has a decimal point in it will be considered as a float in Python due to the fact that decimal points can appear anywhere in a number.

For the most part using floats is okay and your result will be the same as you expect it to be but some times it can be with an arbitrary numbers of decimal places in the result. The arbitrary numbers can be ignored easily. Floats are also the default type if they are used in any calculation in Python, even when it's without a float.
## Large values
If you're working with large numeric values such as millions, you can use underscores to represent the total length of the value.

```Python
universe_age = 14_000_000_000
```

Python will ignore the underscores when it runs your code and this can be done for both integers and floats.

## Related Notes