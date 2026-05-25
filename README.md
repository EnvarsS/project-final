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
- 
---

## Список виконаних завдань

1. **Видалення соціальних мереж VK та Yandex** — прибрано OAuth2-провайдери VK і Yandex (обробники та конфігурацію).

2. **Винесення чутливих даних у змінні оточення** — логін/пароль БД, OAuth2-ключі та налаштування пошти винесено у .env файл.

3. **Перехід на H2 для тестів** — тести тепер використовують H2-database замість PostgreSQL. Додано тестові дані для H2.

5. **Рефакторинг `FileUtil#upload`** — метод переписано з використанням сучасного Java NIO.

6. **Додано підрахунок часу скільки завдання було в роботі та в тестуванні** — методи розрахунку створено в TaskService.

7. **Тести для перевірки правильності роботи ProfileRestController** - створено методи для перевірки методів GET та UPDATE.

8. **Написати Dockerfile для основного сервера**

9. **Написано `docker-compose`** - створено опис інструкцій для створення трьох контейнерів проекту: серверу, БД, nginx 
