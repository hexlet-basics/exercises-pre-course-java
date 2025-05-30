Сложение, конкатенация, нахождение остатка от деления и остальные ранее рассмотренные операции – все это довольно базовые возможности языков программирования.

Математика не ограничена арифметикой, кроме нее есть и множество других разделов со своими операциями — например, геометрия. То же самое касается и строк: их можно переворачивать, менять регистр букв, удалять лишние символы — и это только самое простое. На более высоком уровне есть прикладная логика конкретного приложения.

Программы списывают деньги, считают налоги, формируют отчеты. Количество подобных операций бесконечно и индивидуально для каждой программы. И все они должны быть как-то выражены в коде.

## Как выражаются операции

Для выражения любой произвольной операции в программировании существует понятие **функция**. Функции бывают как встроенные в язык, так и добавленные программистом. С одной встроенной функцией мы уже знакомы — это `println()`.

Функции — одна из ключевых конструкций в программировании, без них невозможно сделать практически ничего. Сначала мы научимся пользоваться уже созданными функциями, а уже потом научимся создавать свои собственные.

Здесь нужно сделать небольшую оговорку. В Java невозможно создать обычную функцию, как это позволяет делать большинство других языков. Все функции Java создаются только внутри классов, которые мы пока не разбирали. А функции, которые определены внутри классов принято называть **методами**. Поэтому в дальнейшем мы будем придерживаться этой терминологии.

Начнем с простых методов для работы над строками. Ниже пример вызова метода `length()`, который считает количество символов в строке:

```java
"Hexlet".length(); // 6
"ABBA".length(); // 4
```

**Методы** — это действия, которые нужно выполнить над данными, к которым они применяются. В программировании **объектами** называют данные, у которых есть методы. В реальности все чуть сложнее, но пока нам достаточно и такого определения. В Java все не примитивные (ссылочные) типы данных — это объекты. Рассмотрим еще несколько примеров с добавлением переменных:

```java
var company = "Hexlet";

var companyLength = company.length();
System.out.println(companyLength); // => 6

// Приводим к верхнему регистру
company.toUpperCase(); // "HEXLET"
```

Основное в работе с методами – понять принцип возврата значения. Методы почти никогда не выводят данные на экран, они их возвращают. Благодаря этому свойству, мы можем разбить нашу программу на кусочки, из которых потом составляется что-то сложное.

В примерах выше результат вызова каждого метода записывается в переменные. Но это не обязательно, мы можем использовать методы напрямую:

```java
var company = "Hexlet";
System.out.println(company.length()); // => 6
```

Постепенно мы начнем знакомиться со все большим количеством встроенных методов в язык. Этих методов настолько много, что их невозможно запомнить. Хорошая новость в том, что это и не требуется. Никто не помнит названий методов наизусть.

Главное — примерно представлять себе, что требуется, а дальше можно использовать подсказки редактора, документацию и Google. Программисты постоянно сидят в документации разбираясь с тем, как что работает.
