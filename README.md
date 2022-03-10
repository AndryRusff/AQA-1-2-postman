## `Статус сборки` [![Build status](https://ci.appveyor.com/api/projects/status/q0deixrkhdv6gwnt?svg=true)](https://ci.appveyor.com/project/AndryRusff/aqa-1-2-postman)
# Тестирование API, CI
## Домашнее задание по курсу "Автоматизированное тестирование"
## Тема: «1.2. Тестирование API, CI», задание №3: «Postman Echo»
### Задача
В этой задаче мы сэмулируем ситуацию, в которой SUT уже запущен, а мы из теста просто обращаемся к нему.
отправка тела запроса:

```java
// Given - When - Then
// Предусловия
given()
  .baseUri("https://postman-echo.com")
  .body("some data") // отправляемые данные (заголовки и query можно выставлять аналогично)
// Выполняемые действия
.when()
  .post("/post")
// Проверки
.then()
  .statusCode(200)
  .body(/* --> ваша проверка здесь <-- */)
;
```

Что нужно сделать:
1. Создайте новый проект на базе Gradle
2. Добавьте необходимые зависимости (если вы не пишите схему, то только rest-assured)
3. Напишите тест, взяв сам запрос из кода выше
4. Изучите ответ и напишите JsonPath-выражение вместо строк `/* --> ваша проверка здесь <--*/`, которое проверит, что в нужном поле хранятся отправленные вами данные (обратите внимание, теперь у вас не массив, а объект).

### Что сделано:
- Применены инструменты:
	- Rest Assured;
	- Сервис Postman Echo.
- Тестируемая функциональность:
	- Удостовериться, что если в запросе будет использоваться неверное JSON выражение, то тесты упадут (в том числе и в CI).
### Предварительные требования
- На компьютере пользователя должна быть установлена Intellij IDEA
### Установка и запуск
1. Склонировать проект на свой компьютер
	- открыть терминал Intellij IDEA
	- ввести команду git clone https://github.com/AndryRusff/AQA-1-2-postman
1. Открыть склонированный проект в Intellij IDEA
1. Запустить авто-тесты во вкладке Terminal (Alt+F12) командой ./gradlew clean test
