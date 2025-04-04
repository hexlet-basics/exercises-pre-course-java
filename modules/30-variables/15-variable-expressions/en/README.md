
Variables are useful not only for storing and reusing information, but also for simplifying complex calculations. Let's look at an example: you need to convert euros to rubles in dollars. Such conversions through an intermediate currency are often made by banks when shopping abroad.

To begin with we will transfer 50 euros to dollars. Suppose that one euro — 1.25 dollars:

```java
var dollarsCount = 50 * 1.25;
System.out.print(dollarsCount);
```

In the previous lesson we wrote down a specific value in a variable. And here `var dollarsCount = 50 * 1.25;` to the right of the sign equals **expression**. The program will calculate the result — `62.5` — and write it into a variable. From the point of view of the program, it does not matter what is in front of him: `62.5` or `50 * 1.25`, both of these options are expressions that need to be calculated. And they are calculated in the same value — `62.5`.

Any string is an expression. String concatenation is also an expression. When the program sees the expression, it processes it and generates the result — **the value of the expression**. Here are some examples of expressions, and in the comments to the right of each expression is the total value:

```java
62.5                         // => 62.5
50 * 1.25                    // => 62.5
120 / 10 * 2                 // => 24
Integer.parseInt("100")      // => 100

"hello"                      // => "hello"
"Good" + "will"              // => "Goodwill"
```

The rules for constructing code (language grammar) are such that in those places where an expression is expected, you can put any calculation (not only mathematical, but also, for example, string — as concatenation), and the program will remain operable. For this reason, it is impossible to describe and show all use cases of all operations.

Programs consist of many combinations of expressions, and understanding this concept is one of the key steps in your path.

Let's return to our monetary program. We write the value of the dollar in rubles, as a separate variable. We calculate the price of 50 euros in dollars, multiplying them by `1.25`. Suppose that 1 dollar — 60 rubles:

```java
var rublesPerDollar = 60;
var dollarsCount = 50 * 1.25; // => 62.5
var rublesCount = dollarsCount * rublesPerDollar; // => 3750

System.out.print(rublesCount);
```

Now let's add text to the output using concatenation:

```java
var rublesPerDollar = 60;
var dollarsCount = 50 * 1.25; // => 62.5
var rublesCount = dollarsCount * rublesPerDollar; // => 3750

System.out.print("The price is" + rublesCount + "rubles");
```


The price is 3750 rubles

Any variable can be part of any expression. At the time of calculation, the value of the variable is substituted for its value.

The value of `dollarsCount` is calculated before it is used in other expressions. When the time comes to use a variable, Java "knows" the value, because it has already calculated it.
