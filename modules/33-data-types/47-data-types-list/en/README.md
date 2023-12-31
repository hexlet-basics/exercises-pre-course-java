
Data types in Java are divided into two important groups according to how variables of this type are related and the values stored in them.

What will the following code output?

```java
var a = 10;
var b = a;
a = 20;
System.out.print(b);
```

10 will be output, because with the assignment b = a, the number 10, which at this moment is contained in a, will be written into the variable b.

If you write

```java
var a = "string";
var b = a;
```

- then the situation will be different.

#### Briefly

Primitive data types in Java:

- Strings in quotes
- The numbers `7`,` -198`, `0` and so on

In fact, there are more, but now let's talk only about them.
---

There are different ways to present data in programs.

There are **strings** - character sets in quotes like `"Hello, World!"`. There are **integers** - for example, `7`, `-198`, `0`. These are two different categories of information - two different **data types**.

The multiplication operation makes sense for integers but it does not make sense for strings: to multiply the word "mother" by the word "notepad" is nonsense.

**The data type determines what can be done with the elements of a specific set of information.**

A programming language recognizes types. Therefore, Java will not allow us to multiply a line by line (“multiply text by text”). But it will allow to multiply an integer by another integer. The presence of types and such restrictions in the language protects programs from random errors.

Unlike strings, numbers do not need to be wrapped in quotes. To print the number 5, just write:

```java
System.out.print(5);
```

Note that the number `5` and the string `"5"` are completely different things, although the output of `println` for this data is identical.

Integers (`1`, `34`, `-19`, etc.) and rational numbers (`1.3`, `1.0`, `-14.324`, etc.) are two separate **types data**. This separation is associated with the characteristics of the device computers. **There are other types**, we will get to know them later.

Here is another example, but with a rational number:

```java
System.out.print(10.234);
```

The lines in programming are called "strings", and the lines of text files are called "lines". For example, the code above has one line (lines), and there are no lines (strings). In all the lessons we will say **string** to indicate the data type "string", and **line** to indicate lines (lines) in files).

Programmers themselves can create new data types, albeit with certain restrictions.
