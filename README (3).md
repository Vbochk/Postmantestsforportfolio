# JSONPlaceholder API Tests — Postman Collection

Коллекция API тестов для публичного REST API [JSONPlaceholder](https://jsonplaceholder.typicode.com/).

## Стек
- Postman
- JSONPlaceholder (публичный тестовый API)

## Покрытые сценарии

| Запрос | Метод | Описание |
|--------|-------|----------|
| GET /posts/1 | GET | Позитивный — получить существующий пост |
| POST /posts | POST | Позитивный — создать новый пост |
| GET /posts/99999 | GET | Негативный — запрос несуществующего поста (404) |

## Тесты

**GET /posts/1:**
- Статус 200
- Время ответа меньше 1000ms
- id равен 1
- Поля title и userId присутствуют в ответе

**POST /posts:**
- Статус 201 Created
- Поле title совпадает с отправленным
- В ответе присвоен id

**GET /posts/99999:**
- Статус 404 Not Found
- Тело ответа пустое

## Как запустить

1. Установить [Postman](https://www.postman.com/downloads/)
2. File → Import → выбрать файл `JSONPlaceholder_API_Tests.json`
3. Открыть коллекцию → выбрать запрос → нажать Send
4. Результаты тестов во вкладке Test Results