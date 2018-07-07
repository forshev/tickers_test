# Тестовое задание

## Getting Started

### Софт

Использовались

```
Python 3.6.2
PostgreSQL 9.6.8
```

### Инструкции

Локально развернуть проект можно так же, как и любой Django-проект.

Реквизиты к базе можно посмотреть/поправить в src/settings.py.

Есть скрипт prepare_python.sh, который создаст виртуальное окружение и установит зависимости.

Парсеры лежат в src/mainapp/management/commands. Миксин для парсеров - в src/mainapp/mixins.py.

Запуск парсеров:

```
python manage.py parse_prices --num_threads=N
```

Если не указать --num_threads, любой парсер запустится в 50 потоков.

Важно сначала запустить parse_tickers, потом можно в любом порядке.

На всякий случай положил в папку дамп моей базы - db.dump.

Функции, возвращающие данные для веб-интерфейсов, лежат в src/mainapp/helper.py

Для API отдельное приложение - src/api