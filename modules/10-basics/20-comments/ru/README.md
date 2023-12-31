Практически все языки программирования позволяют оставлять в коде комментарии. Они никак не используются кодом и нужны исключительно для людей: чтобы программист оставлял пометки для себя и для других программистов.

Комментарии в Java бывают трех видов:

* **Однострочные комментарии** начинаются с `//`. После этих двух символов может следовать любой текст, вся строка не будет анализироваться и исполняться.

    Комментарий может занимать всю строку:

    ```java
    // For Winterfell!
    ```

    Также комментарий может находиться на строке после какого-нибудь кода:

    ```java
    System.out.println("I am the King"); // => For Lannisters!
    ```

* *Многострочные комментарии* начинаются с `/*` и заканчиваются на `*/`. Принято каждую строку начинать с символа `*`, хотя технически это и необязательно:

    ```java
    /*
    * The night is dark and
    * full of terrors.
    */
    System.out.println("I am the King"); // => I am the King
    ```

* **Документирующие комментарии** начинаются с `/**` и заканчиваются на `*/`. Уже для них обязательно каждую строку начинать с символа `*`.

    Документирующие комментарии — это подвид многострочных. При этом несут дополнительную функцию — их можно собрать при помощи специальной утилиты javadoc и выдать в качестве документации к вашему коду. Мы поговорим о них позже – когда разберем классы и методы.
