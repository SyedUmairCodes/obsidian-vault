# Abstract Classes

When you have multiple related classes (like different types of cakes or robots), they often share common features and behaviors. Writing this shared code separately for each class is repetitive and inefficient (like making two cake batters entirely from scratch).

An abstract class acts like a **template or blueprint** for other classes. It allows you to:
- Define shared properties (variables) and methods (functions) that all related classes will use. 
- Specify *what* methods the related classes *must* have, even if the abstract class doesn't know *how* they'll do it.

>[!Note]
>You need to use the `abstract` keyword when creating a abstract class and you **cannot create direct objects** (instances) of an abstract class. It's just a blueprint, not a finished product.

## Related Notes