
The main rule: a variable must be declared before it is used. If you do this later, the program simply will not work.

```java
System.out.print(greeting);
greeting = "Father!";
```

The launch of the program the above ends with an error:

Error: java: cannot find symbol
symbol: variable greeting

This error means that the code uses a variable that is not defined. And in the error itself they say this directly: variable greeting. In addition to the wrong order of definition, in Java there are commonplace typos, both when using a variable and when it is declared.

The number of such errors is reduced by using a properly configured editor. This editor highlights the names that are used without the announcement and warns of possible problems.
