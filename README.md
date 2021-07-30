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
``` 

### Migrate

```
docker-compose run python3 python project/manage.py migrate
```

### Create superuser

```bash
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


### Run server

```
docker-compose up
```

Access [http://localhost:8000](http://localhost:8000)
