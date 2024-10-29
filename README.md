
# Car Management API

Этот проект представляет собой веб-приложение для управления информацией об автомобилях, разработанное с использованием Django и Django REST Framework.

## Установка

1. Клонируйте репозиторий:
   ```bash
   git clone <URL_вашего_репозитория>
   cd car_project
   ```

2. Установите виртуальное окружение:
   ```bash
   python -m venv myenv
   ```

3. Активируйте виртуальное окружение:
   - **Windows**: `myenv\Scripts\activate`
   - **macOS и Linux**: `source myenv/bin/activate`

4. Установите зависимости:
   ```bash
   pip install -r requirements.txt
   ```

5. Выполните миграции базы данных:
   ```bash
   python manage.py migrate
   ```

6. Запустите сервер разработки:
   ```bash
   python manage.py runserver
   ```

## Использование API

- Получение списка автомобилей: `GET /api/cars/`
- Создание нового автомобиля: `POST /api/cars/`
- Получение информации о конкретном автомобиле: `GET /api/cars/<id>/`
- Обновление информации об автомобиле: `PUT /api/cars/<id>/`
- Удаление автомобиля: `DELETE /api/cars/<id>/`

## Авторизация

Для доступа к определенным функциям требуется аутентификация через JWT токены.

1. Получение токена:
   ```bash
   POST /api/token/
   {
      "username": "ваш_логин",
      "password": "ваш_пароль"
   }
   ```

2. Использование токена:
   Добавьте заголовок Authorization к запросам:
   ```
   Authorization: Bearer <ваш токен>
   ```

## Разработчик

[Назар]