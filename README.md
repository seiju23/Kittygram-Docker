#  Kittygram

Это проект, в котором пользователи могут загружать фотографии своих котов и делиться их достижениями.

## Как запустить проект

Клонируем репозиторий: 

```bash 
git clone git@github.com:seiju23/Kittygram-Docker.git
```

Запускаем контейнеры:

```bash
sudo docker compose -f docker-compose.production.yml up -d
```

Делаем миграции, собираем статику:

```bash
sudo docker compose -f docker-compose.production.yml exec backend python manage.py migrate

sudo docker compose -f docker-compose.production.yml exec backend python manage.py collectstatic

sudo docker compose -f docker-compose.production.yml exec backend cp -r /app/collected_static/. /static/static/
```

Проект будет доступен по адресу:

```
http://localhost:9000/
```

## Использованные технологии

- Python
- Django
- Django REST framework
- JavaScript
- Nginx
- Docker
- Github Actions

## Об авторе:

Равлис Игорь (tg: @seiju23, email: seiju.pioneer23@gmail.com)
