# Introduction to Java

Java is a widely-used, object-oriented programming (OOP) language. It's used in everything from mobile phones to enterprise applications. Key features include robust error handling, a rich standard library, and a strong community.

Java code is re-useable, Java code is compiled into something called bytecode. This bytecode runs on the Java Virtual Machine (JVM). As long as a device has a JVM, it can run Java code, regardless of the underlying operating system.

Java has a structured way to deal with errors (exceptions) that occur during program execution. This prevents crashes and allows your program to recover gracefully. Java automatically manages memory allocation and deallocation. You don't have to worry about manually freeing up memory you're no longer using (like you do in C/C++). This prevents memory leaks, a common source of bugs.

The Java standard library is a massive collection of pre-built classes and methods that you can use in your programs.

```Java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, world!");
    }
}
```

## Related Notes