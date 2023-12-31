
```java
"Hello"
"Goodbye"

"G"
" "
""
```

Which of these five options are strings?

Everything is clear with the first two, these are exactly strings, we have already worked with similar constructions and said that strings are character sets.

Any single character in quotes is a string. The empty string `" "` is also a string. That is, we consider everything to be inside the quotes, even if it is a space, one character or no characters at all.

Imagine that you want to print _dragon's mother_ line. The apostrophe before the letter **s** is the same character as a single quote. Let's try:

This version of the program will work correctly:

```java
System.out.println("Dragon's mother");
```
  
And what if we want to create such a string:

```
Dragon's mother said "No"
```

It contains both single and double quotes. How to be in this situation?

To do this, use the **escape character**: `\`. If you put `\` before the quotation mark (single or double), it will mean that the quotation mark should be viewed not as the beginning or end of the line, but as part of the line.

```java
System.out.println("Dragon's mother said \"No\"");
```
