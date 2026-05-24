## [REST API](http://localhost:8080/doc)

## Концепция:

- Spring Modulith
    - [Spring Modulith: достигли ли мы зрелости модульности](https://habr.com/ru/post/701984/)
    - [Introducing Spring Modulith](https://spring.io/blog/2022/10/21/introducing-spring-modulith)
    - [Spring Modulith - Reference documentation](https://docs.spring.io/spring-modulith/docs/current-SNAPSHOT/reference/html/)

```
  url: jdbc:postgresql://localhost:5432/jira
  username: jira
  password: JiraRush
```

- Есть 2 общие таблицы, на которых не fk
    - _Reference_ - справочник. Связь делаем по _code_ (по id нельзя, тк id привязано к окружению-конкретной базе)
    - _UserBelong_ - привязка юзеров с типом (owner, lead, ...) к объекту (таска, проект, спринт, ...). FK вручную будем
      проверять

## Аналоги

- https://java-source.net/open-source/issue-trackers

## Тестирование

- https://habr.com/ru/articles/259055/

Список выполненных задач:
1. Видалення соціальних мереж VK та Yandex — прибрано OAuth2-провайдери та представлення для VK і Yandex.
2. Винесення чутливих даних у .env файл — логін/пароль БД, OAuth2-ключі та налаштування пошти винесено у .env файл.
3. Перехід на H2 для тестів — тести тепер використовують H2-database. Додано тестові дані для H2.
4. Рефакторинг FileUtil#upload — метод переписано з використанням сучасного Java NIO.
