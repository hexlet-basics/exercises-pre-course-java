
We want to show the dialogue of the Mother of Dragons with her child:

```
- Are you hungry?
- Aaaarrrgh!
```

If you display a line with the following text:

```java
System.out.print("— Are you hungry?— Aaaarrrgh!");
```

it will turn out like this:

```
— Are you hungry?— Aaaarrrgh!
```

We need to somehow tell the interpreter "click on enter" — to make a line break after the question mark.

In Java, `\n` is a line break:

```java
System.out.print("— Are you hungry?\n— Aaaarrrgh!");
```

result:

```
— Are you hungry?
— Aaaarrrgh!
```

`\n` is an example **of the escape sequence** (escape sequence). They are also called control structures.

While typing in some Word, you press Enter at the end of the line. The editor puts a special invisible character at the end of the line, which is called LINE FEED (LF). In some editors, you can even turn on the display of invisible characters. Then the text will look something like this:

```
— Hello!¶
— Oh, hi!¶
— How are you?
```

A device that outputs the corresponding text takes this symbol into account. For example, the printer, when meeting with LF, pulls the paper up one line, and the text editor transfers all subsequent text below, also one line.

Although there are more than a dozen of such characters, there are often only a few in programming. In addition to line breaks, these characters include tabulation (a break, obtained by pressing the Tab button) and carriage returnValue (only in Windows). We, programmers, often need to use, for example, the translation of the string `\n` to properly format the text.

```java
System.out.print("Gregor Clegane\nDunsen\nPolliver\nChiswyck");
```

**Attention! Escaping sequences like `\n` work only inside double quotes!**

The screen will display:

```
Gregor Clegane
Dunsen
Polliver
Chiswyck
```

For convenience, there is a method `System.out.println`, which allows you to display some value on the console and then transfer the console to the next line. For example:

```java
System.out.println("Hello");
System.out.println("World");
```
The screen will display:

```
Hello
World
```

Pay attention to the following points:

1\. It does not matter what comes before or after `\n`: a character or an empty string. The transfer will be detected and executed in any case.

2\. Remember that a string can contain only one character or zero characters at all? And the line can contain only `\n`:

```java
System.out.print("Gregor Clegane");
System.out.print("\n");
System.out.print("Dunsen");
```

Here we print one line with the name, then one line “line feed”, and then another line. The program will display:

```
Gregor Clegane
Dunsen
```

3\. Despite the fact that in the source code of a program, a sequence of type `\n` looks like two characters, from the point of view of the interpreter it is a special single character.

4\. If we need to display `\n` exactly as text (two separate printable characters), then we can use the already known screening method, adding one more `\` at the beginning. That is, the sequence `\\n` is displayed as the characters `\` and `n` following each other.

```java
System.out.print("Joffrey loves using \\n");
```

the screen will be released:

```
Joffrey loves using \n
```

A small but important note about Windows. On Windows, `\r\n` is used to translate strings by default. Such a combination works well only in Windows, but creates problems when transferring to other systems (for example, when the development team has both Windows and Linux users). The fact is that the sequence `\r\n` has a different interpretation depending on the selected encoding (discussed later). For this reason, in the development environment, it is customary to always use `\n` without `\r`, since LF is always treated the same way and works fine in any system. Remember to configure your editor to use `\n`.
