## `Статус сборки` [![Build status](https://ci.appveyor.com/api/projects/status/q0deixrkhdv6gwnt?svg=true)](https://ci.appveyor.com/project/AndryRusff/aqa-1-2-postman)
# Тестирование API, CI
## Домашнее задание по курсу "Автоматизированное тестирование"
## Тема: «1.2. Тестирование API, CI», задание №3: «Postman Echo»
- Применены инструменты:
	- Rest Assured;
	- Сервис Postman Echo.
- Тестируемая функциональность:
	- Удостовериться, что если в запросе будет использоваться неверное JSON выражение, то тесты упадут (в том числе и в CI).
### Предварительные требования
- На компьютере пользователя должна быть установлена Intellij IDEA
### Установка и запуск
1. Склонировать проект на свой компьютер
	- открыть терминал
	- ввести команду 
		```
		git clone https://github.com/AndryRusff/AQA-1-2-postman
		```
1. Открыть склонированный проект в Intellij IDEA
1. Запустить авто-тесты В Intellij IDEA во вкладке Terminal (Alt+F12) командой ./gradlew clean test
