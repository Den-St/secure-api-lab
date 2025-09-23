# Лабораторно-практична робота №3

## Загальний опис

Застосунок, створений на Node.js, реалізує простий REST API для збереження та отримання інформації.  
Основний функціонал включає базові операції: перегляд усіх записів та додавання нових.  
Проєкт слугує навчальним прикладом роботи з HTTP-запитами, використання залежностей та налаштування змінних оточення.

## Встановлення залежностей

npm install

## Структура проєкту

-   `server.js` --- сервер
-   `package.json` --- опис залежностей і скриптів
-   `test-client.js` --- тестування роботи
-   `data.js` --- дані, що використовуються

## Залежності

-   залежності вказані у `package.json` (express)

## Скрипти

-   `npm start` --- запуск застосунку
-   `npm test` --- запуск тестів

## API ендпоінти

| Метод | URL | Опис | Заголовки | Тіло запиту | Можливі відповіді |
|-|-|-|-|-|-|
| GET   | /documents| Отримати всі дані|Authorization: <br>x-login,<br> x-password|—| **200 OK** – список даних<br>**401 Unauthorized** – відсутня/неправильна авторизація|
|POST|/documents|Додати новий запис|Authorization: <br>x-login,<br> x-password|{ "title": "Q3 Financial Report", "content": "The financial results for Q3 are positive."}| **201 Created** – запис додано<br>**400 Bad Request** – некоректні дані<br>**401 Unauthorized**|
|GET|/employees|Oтримання списку всіх співробітників|Authorization: <br>x-login,<br> x-password|—|**200 OK** – список даних<br>**401 Unauthorized**<br>**403 Access denied** - недостатньо прав|
| DELETE|/documents/:id|Видалити запис за ID|Authorization: <br>x-login,<br> x-password|—|**204 No Content** – запис видалено<br>**404 Not Found** – запис не знайдено<br>**401 Unauthorized**|



<img width="1280" height="793" alt="image1" src="https://github.com/user-attachments/assets/b081fc7b-8651-4376-8f76-42ea5157b337" />
<img width="1275" height="796" alt="image2" src="https://github.com/user-attachments/assets/07c83f2c-6ab9-48a5-b9c2-dc34350e7cb1" />
<img width="1269" height="796" alt="image3" src="https://github.com/user-attachments/assets/a09579c3-11cf-403f-8dd6-203501ac7bda" />
<img width="1269" height="793" alt="image4" src="https://github.com/user-attachments/assets/9b30f7c2-4755-482c-b9be-147206b06438" />
