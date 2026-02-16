# Локальный запуск Postman CRUD коллекции

## Что внутри
- `Book_CRUD.postman_collection.json` — коллекция с 5 CRUD-запросами к локальному API книг.
- `Book_CRUD.postman_environment.json` — окружение с `userId` и переиспользуемыми переменными.

## Важно
Коллекция настроена на **локальный** сервис:
- `baseUrl = http://localhost:3000` (переменная на уровне коллекции)
- эндпоинты: `/books`, `/books/:id`

Если у вас другой порт/путь — поменяйте `baseUrl` в коллекции.

## Требования
- Локально запущенный API на `http://localhost:3000` с CRUD для `books`.
- Приложение Postman (Desktop/Web).

## Как запустить
1. Откройте Postman.
2. Импортируйте файлы:
   - `postman/Book_CRUD.postman_collection.json`
   - `postman/Book_CRUD.postman_environment.json`
3. Выберите Environment: **Book CRUD Local Environment**.
4. Откройте коллекцию **Book CRUD Basic Checks**.
5. Нажмите **Run collection** и запустите все 5 запросов.

## Ожидаемый результат
После запуска всей коллекции:
- выполняются все 5 запросов (Create, Read all, Read one, Update, Delete);
- каждый запрос содержит минимум 2 проверки;
- в каждом запросе есть проверка response time;
- переменные (`userId`, `bookId`, `bookTitle`, `createdBookId`) сохраняются и переиспользуются.
