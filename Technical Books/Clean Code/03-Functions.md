# Clean Functions

When writing functions using clean code always remember:

- Keep the function small.
- One function per task.

This implies that the code blocks within your if-else and while statements should be less than three lines long. The ideal way to create functions is that they shouldn't have any arguments in them but in most cases you'll have to pass one or two arguments in your functions.

> Your functions will have side effects although your functions only do one thing but they also do many hidden things like changing the values of variables or passing them as global.

Some functions can also have output arguments arguments in functions are used for input but they sometimes can also be used for outputs as well.

Making switch statements is much harder than functions because they always perform N number of things. If you really want to make them smaller you use them in low-level classes using poly-morphism.

Try-catch blocks confuse the structure of the code and mix error processing with normal processing so it is better to extract the bodies of the try and catch blocks out into functions of their own.

## Related Notes