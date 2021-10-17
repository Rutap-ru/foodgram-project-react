### Описание
Приложение «Продуктовый помощник»: сайт, на котором пользователи могут публиковать рецепты, добавлять чужие рецепты в избранное и подписываться на публикации других авторов.
Сервис «Список покупок» позволит перед походом в магазин скачивать сводный список продуктов, необходимых для приготовления одного или нескольких выбранных блюд.


#### Найти проект можно по этому адресу: 
http://178.154.217.239
* Админка: http://178.154.217.239/admin/
* Логин: admin
* Пароль: 123456789

### Технологии:
* Python 3.8.5
* Django 3.2.5
* Django rest framework 3.11.0
* Gunicorn 20.1.0
* Nginx 1.19.3
* Postgres 12.4

### Команды для работы с приложением:
-  Клонировать приложение к себе в репозиторий
```bash
git clone https://github.com/rutap/foodgram-project-react.git
```
- Необходимые переменные окружения, сохраненные в .env
    - DB_ENGINE
    - DB_NAME
    - POSTGRES_USER
    - POSTGRES_PASSWORD
    - DB_HOST
    - DB_PORT

- Запуск приложения
```bash
docker-compose up -d --build
```
- Сделать миграции
```bash
sudo docker-compose exec backend python manage.py makemigrations

sudo docker-compose exec backend python manage.py migrate --noinput
```
- Создание суперпользователя
```bash
sudo docker-compose exec backend python manage.py createsuperuser
```
- Подготовка статики проекта
```bash
sudo docker-compose exec backend python manage.py collectstatic --no-input
```
- Загрузка подготовленненных данных (ингредиенты)
```bash
sudo docker-compose exec backend python manage.py loaddata data/ingredients.json
```
### Авторы
Николай, студентк факультета Бэкэнд Яндекс.Практикум

