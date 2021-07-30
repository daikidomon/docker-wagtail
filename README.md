# Docker

## Initial Setting

### Make dir & Build container

```bash
mkdir src
docker-compose build --no-cache
```

### Create project

```
docker-compose run python3 wagtail start project
docker-compose run python3 python project/manage.py migrate
``` 

### Check runserver

http://localhost:8000

## Migration & Create superuser

### Migrate

```
docker-compose run python3 python manage.py migrate
```

### Create superuser

```
docker-compose run python3 python manage.py createsuperuser
```

Interactive input.

```
Username (leave blank to use 'root'): root 
Email address: root@sample.com
Password:
Password (again):
Superuser created successfully.
```

## Create App

```
docker-compose run python3 python manage.py startapp cms
```
