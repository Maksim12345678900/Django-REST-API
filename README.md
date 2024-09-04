# Warehouse Management Project

## Описание
Проект для управления складом с использованием Django и Django REST Framework. Включает регистрацию пользователей, создание складов и товаров, а также операции поставки и потребления товаров.

## Запуск проекта

1. Создайте виртуальное окружение:
    ```bash
    python -m venv venv
    ```

2. Активируйте виртуальное окружение:
    - Windows: `venv\Scripts\activate`
    - MacOS/Linux: `source venv/bin/activate`

3. Установите зависимости:
    ```bash
    pip install -r requirements.txt
    ```

4. Примените миграции:
    ```bash
    python manage.py migrate
    ```

5. Запустите сервер:
    ```bash
    python manage.py runserver
    ```

## Тестирование проекта

### URL

- Регистрация пользователя: `POST /api/users/`
- Создание склада: `POST /api/warehouses/`
- Создание товара: `POST /api/products/`
- Поставка товара: `POST /api/supplies/`
- Потребление товара: `POST /api/consumptions/`

### Примеры данных для тестирования

- **Регистрация пользователя**:
    ```json
    {
        "username": "supplier1",
        "email": "supplier1@example.com",
        "password": "password123",
        "user_type": "supplier"
    }
    ```

- **Создание склада**:
    ```json
    {
        "name": "Main Warehouse"
    }
    ```

- **Создание товара**:
    ```json
    {
        "name": "Product A",
        "quantity": 100,
        "warehouse": 1
    }
    ```

- **Поставка товара**:
    ```json
    {
        "supplier": 1,
        "product": 1,
        "quantity": 50
    }
    ```

- **Потребление товара**:
    ```json
    {
        "consumer": 1,
        "product": 1,
        "quantity": 20
    }
    ```
