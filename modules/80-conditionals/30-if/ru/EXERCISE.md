
Реализуйте метод `getSentenceTone()`, который принимает строку и определяет тон предложения. Если все символы в верхнем регистре, то это вопль — `scream`. В ином случае — нормальное предложение — `normal`.

Примеры вызова:

```java
App.getSentenceTone("Hello"); // "normal"
App.getSentenceTone("WOW");  // "scream"
```

Алгоритм:

1. Сгенерируйте строку в верхнем регистре на основе строки-аргумента с помощью `toUpperCase()`.
2. Сравните её с исходной строкой:
    * Если строки равны, значит, строка-аргумент в верхнем регистре
    * В ином случае — строка-аргумент не в верхнем регистре
