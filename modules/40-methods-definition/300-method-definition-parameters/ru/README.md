Методы могут не только возвращать значения, но и принимать их в виде параметров. С параметрами методов мы уже сталкивались много раз:

```java
// Принимает на вход один параметр любого типа
System.out.println("я параметр");
// Принимает на вход индекс, по которому извлекается символ
"какой-то текст".charAt(3); // 'о'
// Принимает на вход два строковых параметра
// Первый — что ищем, второй — на что меняем
"google".replace("go", "mo"); // "moogle"
// Принимает на вход два числовых параметра
// первый — начальный индекс включительно, второй — конечный индекс не включительно
"hexlet".substring(1, 3); // "ex"
```

В этом уроке мы научимся создавать методы, которые принимают на вход параметры.

Представим, что перед нами стоит задача — реализовать статический метод `App.getLastChar()`. Он должен возвращать последний символ в строке, переданной на вход как параметр.

Вот как будет выглядеть использование этого метода:

```java
// Передача параметров напрямую без переменных
App.getLastChar("Hexlet"); // 't'
App.getLastChar("Goo"); // 'o'
// Передача параметров через переменные
var name1 = "Hexlet";
App.getLastChar(name1); // 't'
var name2 = "Goo";
App.getLastChar(name2); // 'o'
```

Из описания и примеров кода мы можем сделать следующие выводы:

* Нам нужно определить статический метод `getLastChar()` в классе `App`
* Метод должен принимать на вход один параметр типа `String`
* Метод должен возвращать значение типа `char`

Для начала определим метод:

```java
class App {
    public static char getLastChar(String str) {
        // Вычисляем индекс последнего символа как длина строки, то есть 1
        return str.charAt(str.length() - 1);
    }
}
```

Разберем этот код подробнее. `char` говорит нам о типе возвращаемого значения. Далее в скобках указывается тип параметра `String` и его имя `str`.

Внутри метода мы не знаем, с каким конкретно значением идет работа, поэтому параметры всегда описываются как переменные.

Имя параметра может быть любым — оно не связано с тем, как вызывается метод. Главное, чтобы это имя отражало смысл того значения, которое содержится внутри. Конкретное значение параметра будет зависеть от вызова этого метода.

Параметры в Java всегда обязательны. Если методу нужны параметры, а мы попробуем написать код без параметра, то компилятор выдаст ошибку:

```sh
App.getLastChar(); // такой код не имеет смысла
method getLastChar in class App cannot be applied to given types;
  required: String
  found:    no arguments
  reason: actual and formal argument lists differ in length
```

Точно таким же образом можно указывать два и более параметра. Каждый параметр отделяется запятой:

```java
class App {
    // Метод по нахождению среднего числа
    // Возвращаемый тип — double, потому что
    // при делении может получиться дробное число
    public static double average(int x, int y) {
        return (x + y) / 2.0;
    }
}

App.average(1, 5); // 3.0
App.average(1, 2); // 1.5
```

Методы могут требовать на вход любое количество параметров, которое им нужно для работы:

```java
// первый параметр – что ищем
// второй параметр – на что меняем
'google'.replace('go', 'mo'); // moogle
````

Для создания таких методов, нужно в определении указать нужное количество параметров через запятую, дав им понятные имена. Ниже пример определения метода `replace()`, который заменяет в слове одну часть строки на другую:

```java
class App {
    public static String replace(String text, String from, String to) {
        // здесь тело метода, но мы его
        // опускаем, чтобы не отвлекаться
    }
}

App.replace('google', 'go', 'mo'); // moogle
```

Когда параметров два и более, то практически для всех методов становится важен порядок передачи этих параметров. Если его поменять, то метод отработает по-другому:

```java
// ничего не заменилось,
// так как внутри google нет mo
App.replace('google', 'mo', 'go'); // google
```
