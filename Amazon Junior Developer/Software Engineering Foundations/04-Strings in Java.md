# Strings in Java

Strings are sequences of characters used to represent text. They are *immutable* (cannot be changed after creation). Strings are objects and have built-in methods for manipulation. Characters in a string have an index (position) starting from 0.

A String is "represented internally as an array of the char data type."  This is a good way to visualize it.  Think of `"Java"` as being like `{'J', 'a', 'v', 'a'}` internally. However, you don't *directly* interact with this underlying `char` array. You use String methods.

```java
String message = "Hello";
message = message + " world!"; // A *new* String object is created
// The original "Hello" String object still exists (and can be garbage collected)
System.out.println(message); // Prints "Hello world!"
```

> Immutable objects are inherently thread-safe. Multiple threads can access the same String without worrying about concurrent modification issues.

Java uses a "String pool" to store String literals.  If you create multiple String literals with the same value, they all point to the *same* object in the pool.  This saves memory.  Immutability makes this optimization possible.



```java
public class StringExamples {
	public static void main(String[] args) {
		String name = "Alice";

	// Immutability
		String upperName = name.toUpperCase(); // Creates a *new* String
		System.out.println(name);       // Prints "Alice" (original unchanged)
		System.out.println(upperName);  // Prints "ALICE"

	// charAt()
		char firstChar = name.charAt(0); // 'A'
		char lastChar = name.charAt(name.length() - 1); // 'e'
		System.out.println("First char: " + firstChar);
		System.out.println("Last char: " + lastChar);

	// length()
		int nameLength = name.length();
		System.out.println("Length: " + nameLength); // 5

	// StringIndexOutOfBoundsException (Example of an error)
	// char invalidChar = name.charAt(5); // This would cause an exception
        }
    }
    ```

## Common String Methods


```java
public class StringMethodExamples {
	public static void main(String[] args) {
		String text = "Hello, World!";

	// length() - Returns the number of characters in the string.
		int len = text.length(); // len is 13

	// charAt(index) - Returns the character at the specified index (0-based).
		char firstChar = text.charAt(0); // firstChar is 'H'
		char lastChar = text.charAt(len - 1); // lastChar is '!'

	// substring(beginIndex) - Returns a new string starting from beginIndex to the end.
		String world = text.substring(7); // world is "World!"

	// substring(beginIndex, endIndex) - Returns a new string from beginIndex (inclusive) to endIndex (exclusive).
		String hello = text.substring(0, 5); // hello is "Hello"

	// equals(otherString) - Compares two strings for equality (case-sensitive).  Returns a boolean.
		boolean isEqual = text.equals("Hello, World!"); // isEqual is true
		boolean isEqual2 = text.equals("hello, world!"); // isEqual2 is false (case-sensitive)

	// equalsIgnoreCase(otherString) - Compares two strings, ignoring case.
		boolean isEqualIgnoreCase = text.equalsIgnoreCase("hello, world!"); // isEqualIgnoreCase is true

	// toLowerCase() - Returns a new string with all characters converted to lowercase.
		String lower = text.toLowerCase(); // lower is "hello, world!"

	// toUpperCase() - Returns a new string with all characters converted to uppercase.
		String upper = text.toUpperCase(); // upper is "HELLO, WORLD!"

	// contains(sequence) - Returns true if the string contains the specified sequence of characters.
		boolean containsWorld = text.contains("World"); // containsWorld is true
		boolean containsJava = text.contains("Java"); // containsJava is false

	// replace(oldChar, newChar) - Returns a new string with all occurrences of oldChar replaced by newChar.
		String newText = text.replace('o', '0'); // newText is "Hell0, W0rld!"

	// replace(oldSequence, newSequence)
		String newerText = text.replace("World", "Java"); //newerText is Hello, Java!

	// trim() - Returns a new string with leading and trailing whitespace removed.
		String spacedText = "   Hello   ";
		String trimmedText = spacedText.trim(); // trimmedText is "Hello"

	// indexOf(char) - Returns the index of the *first* occurrence of the specified character, or -1 if not found.
		int indexOfO = text.indexOf('o'); // indexOfO is 4

	// indexOf(char, fromIndex) - Starts searching from the specified index.
		int indexOfOFrom5 = text.indexOf('o', 5); // indexOfOFrom5 is 8

	// lastIndexOf(char) - Returns the index of the *last* occurrence of the character.
		int lastIndexOfO = text.lastIndexOf('o'); // lastIndexOfO is 8

	// startsWith(prefix) - Returns true if the string starts with the specified prefix.
		boolean startsWithHello = text.startsWith("Hello"); // startsWithHello is true

	// endsWith(suffix) - Returns true if the string ends with the specified suffix.
		boolean endsWithExclamation = text.endsWith("!"); // endsWithExclamation is true

	// split(regex) - Splits the string into an array of strings based on the given regular expression (delimiter).
		String sentence = "This is a sentence.";
		String[] words = sentence.split(" "); // words is {"This", "is", "a", "sentence."}

	// isEmpty() - Returns `true` if the string is empty (length is 0), `false` otherwise.
		String emptyString = "";
		boolean isEmpty = emptyString.isEmpty(); // isEmpty is true
		boolean isNotEmpty = text.isEmpty();    // isNotEmpty is false

	 // String.valueOf()  - Converts different types of values (like int, double, boolean) to their String representation.
		int number = 123;
		String numberString = String.valueOf(number); // numberString is "123"

		double pi = 3.14159;
		String piString = String.valueOf(pi); // piString is "3.14159"
        }
    }
    ```

**String Concatenation**
Concatenation joins strings together. The `+` operator is used for concatenation. If you use `+` with numbers and strings, be careful about the order of operations (use parentheses).

`+` can be used in `println` statements to combine strings and variables. The `+` operator is "overloaded" in Java.  This means it has different meanings depending on the context:
*   With numbers, it performs addition.
*   With at least one `String` operand, it performs concatenation.

**StringBuilder and StringBuffer:**  
For *repeated* concatenation within a loop, using the `+` operator can be inefficient because it creates many intermediate String objects.  In these cases, `StringBuilder` (or `StringBuffer` for thread-safe situations) is much more efficient.  

```java
public class ConcatenationExamples {
	public static void main(String[] args) {
		String firstName = "Alice";
		String lastName = "Smith";

	// Basic concatenation
		String fullName = firstName + " " + lastName; // "Alice Smith"
		System.out.println(fullName);

	// Concatenation with numbers (order of operations)
		int x = 10;
		int y = 5;
		System.out.println("Sum: " + x + y);       // "Sum: 105" (concatenation)
		System.out.println("Sum: " + (x + y));     // "Sum: 15" (addition first)

	// Using StringBuilder for efficiency (in a loop)
		StringBuilder sb = new StringBuilder();
		for (int i = 0; i < 1000; i++) {
			sb.append(i); // Efficiently appends to the StringBuilder
			sb.append(" ");		}
		String result = sb.toString(); // Convert to a String
	//System.out.println(result);

	//Concatenation using + inside print
		System.out.println("Hello my name is " + fullName + "and I scored " + (x + y) + "on my test.");
        }
    }
    ```

## Related Notes
