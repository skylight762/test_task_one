## тестовое задание

- написать RESTful сервис, цель которого - операции со счетами пользователей.


- Должно быть как минимум 3 метода:

  1)перевод денег с одного счёта на другой

  2)положить деньги на счёт

  3)снять деньги со счёта.

- Отрицательный баланс счета недопустим.

В качестве хранилища можно использовать любую in-memory БД. Доступ к БД осуществить через JPA. Исходный код должен
собираться с помощью maven или gradle в исполняемый jar. Решение должно быть на Spring (Java) Если в инструкции не
хватает каких-то данных, то дополнить задание можно на свое усмотрение и описать все иходные данные в README. Проект
разметсить на github

- в качестве in-memory DB используется h2, доступна консоль
```
http://localhost:8080/h2-console 
login = user, password = password 
```
- валидация балланса на счете реализована в классе.

```
src/main/java/com/example/test_task/validation/CustomValidator.java
```

- для тестирования можно использовать файл http запросов

```
dev/http/test.http
```

- или swagger UI

```
http://localhost:8080/swagger-ui
```

- вывод сообщений с результатами операций реализован через log.info в консоль

- результаты завершенных транзакций сохраняются в таблицу transaction с информацией: номер счета, тип операции, сумма, время начала операции, время окончания операции