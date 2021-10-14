### Описание/ Description
Приложение «Продуктовый помощник»: сайт, на котором пользователи могут публиковать рецепты, добавлять чужие рецепты в избранное и подписываться на публикации других авторов.
Сервис «Список покупок» позволит перед походом в магазин скачивать сводный список продуктов, необходимых для приготовления одного или нескольких выбранных блюд.
***
"Product Assistant" app: a site where users can post recipes, add other people's recipes to favorites, and subscribe to other authors' publications.
The "Shopping List" service will allow you to download a consolidated list of products required to prepare one or several selected dishes before going to the store. 

#### Найти проект можно по этому адресу/ Web address: 


### Технологии/ Technology:
* Python 3.8.5
* Django 3.2.5
* Django rest framework 3.11.0
* Gunicorn 20.1.0
* Nginx 1.19.3
* Postgres 12.4

### Команды для работы с приложением/ How to start:
-  Клонировать приложение к себе в репозиторий/ Clone the app to your repository
```bash
git clone https://github.com/rutap/foodgram-project-react.git
```
- Необходимые переменные окружения, сохраненные в .env/ Required environment variables saved in .env
    - DB_ENGINE
    - DB_NAME
    - POSTGRES_USER
    - POSTGRES_PASSWORD
    - DB_HOST
    - DB_PORT

- Запуск приложения/ App launch
```bash
docker-compose up -d --build
```
- Сделать миграции/ Make migrations
```bash
docker-compose exec backend python manage.py makemigrations

docker-compose exec backend python manage.py migrate --noinput
```
- Создание суперпользователя/ Create superuser
```bash
docker-compose exec backend python manage.py createsuperuser
```
- Подготовка статики проекта/ Preparing project statics
```bash
docker-compose exec backend python manage.py collectstatic --no-input
```
- Загрузка подготовленненных данных (ингредиенты)/ Loading prepared data (ingredients)
```bash
docker-compose exec backend python manage.py loaddata data/ingredients.json
```
### Авторы/ Author
Николай, студентк факультета Бэкэнд Яндекс.Практикум/ Nikolay, Yandex.Practicum student

