
Реализуйте метод `normalizeUrl()`, который выполняет так называемую нормализацию данных. Он принимает адрес сайта и возвращает его с *https://* в начале.

Метод принимает адреса в виде *АДРЕС* или *https://АДРЕС*, но всегда возвращает адрес в виде *https://АДРЕС*

Можно использовать метод `startsWith()` чтобы проверить начинается ли строка с префикса *https://*. А потом на основе этого добавлять или не добавлять *https://*.

```java
App.normalizeUrl("google.com"); // "https://google.com"
App.normalizeUrl("https://ai.fi"); // "https://ai.fi"
```
