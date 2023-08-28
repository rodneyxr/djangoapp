# Quickstart

Start the postgres database

```sh
docker-compose up -d
```

Run the migrations

```sh
docker-compose run --rm web python manage.py makemigrations
docker-compose run --rm web python manage.py migrate
```

Create an `admin` user

```sh
docker-compose run --rm web python manage.py createsuperuser
```

Test it out

```sh
http://localhost:8000
http://localhost:8000/admin
```