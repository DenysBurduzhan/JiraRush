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
1. Understand the project structure (onboarding).
2. Removed VK and Ya.
3. Introduce sensitive information to a specific file.
4. Change of tests from PostgreSQL to in-memory database.
5. Write tests for all public methods of the ProfileRestController controller.
6. Refactor the com.javarush.jira.bugtracking.attachment.FileUtil#upload method to use a modern approach to working with the file system.
7. Add new functionality: adding tags to a task (REST API + implementation on the service).
8. Add time counting: how much time the task has been in work and testing. Write 2 methods at the service level that take a task as a parameter and return the time spent.