# Отслеживатель задач

Приложение для отслеживания ежедневных задач, созданное на базе **Laravel 12** и **Livewire 4 (Volt)**.

# Функции TaskTracker##

- **Навигация по календарю**: Просмотр задач по дням с помощью интуитивно понятного 7-дневного календаря и средства выбора дат
- **Управление ежедневными задачами**: Создание, редактирование, завершение и удаление задач с указанием приоритетов, категорий и тегов.
- **Фильтры**: Поиск, фильтрация по статусу (все / завершено /незавершенно), категории и приоритету
- **Панель мониторинга**: Обзор текущего прогресса, еженедельная статистика, счетчик просроченных предупреждений
- ** Статистика и тепловые карты **: тепловая карта активности за 90 дней, тенденции завершения, распределение приоритетов, производительность по дням недели, разбивка по категориям, облако тегов
- **Аутентификация**: Полный процесс авторизации с помощью Laravel Breeze (логин, регистрация, сброс пароля, проверка электронной почты)
- **Доступ на основе ролей**: Роли администратора и пользователя с детализированными разрешениями с помощью Spatie Laravel Permission

## Технический стек

- Laravel 12 / PHP 8.4
- Livewire 4.1 (Volt functional components)
- Tailwind CSS 4 with Inter font
- SQLite (default, swappable)
- Laravel Breeze (Livewire scaffold)
- Spatie Laravel Permission 6.x

## Установка проекта

```bash
composer install
npm install
cp .env.example .env
php artisan key:generate
touch database/database.sqlite
php artisan migrate --seed
npm run build
php artisan serve
```

## Тестовые аккаунты

| Email             | Password | Role  |
|-------------------|----------|-------|
| admin@example.com | password | admin |
| test@example.com  | password | user  |
| demo@example.com  | password | user  |

## Страницы

| Route        | Description                                    |
|--------------|------------------------------------------------|
| `/`          | Landing page                                   |
| `/dashboard` | Overview with stats, overdue/upcoming tasks     |
| `/tasks`     | Daily task view with calendar bar and CRUD      |
| `/statistics`| Analytics: heatmap, trends, charts, tag cloud   |
| `/profile`   | User profile settings                          |

## Документация

See [`.docs/IMPLEMENTATION.md`](.docs/IMPLEMENTATION.md) for architecture details and [`.docs/CHANGES.md`](.docs/CHANGES.md) for changelog.
