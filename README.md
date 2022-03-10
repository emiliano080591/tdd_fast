# FastApi example

Ejemplo de un api con FastApi, docker y CI

### Levantar servidor manualmente

```shell
$ >  uvicorn app.main:app --reload
```

### Crear imagen docker

```shell
$ >  docker-compose build
```

### Levantar imagen docker

```shell
$ >  docker-compose up -d
```
### Construir y levantar imagen docker

```shell
$ >  docker-compose up -d --build
```

### Bajar imagen docker

```shell
$ >  docker-compose down
```

### Iniciar primera migracion

```shell
$ >  docker-compose exec web aerich init -t app.db.TORTOISE_ORM
```

### Crear primera migracion

```shell
$ >  docker-compose exec web aerich init-db
```

### Correr tests

```shell
$ >  docker-compose exec web python -m pytest
```

### Correr tests con coverage

```shell
$ >  docker-compose exec web python -m pytest --cov="."
```

### Generar reporte de los tests(html)

```shell
$ >  docker-compose exec web python -m pytest --cov="." --cov-report html
```

### Correr el quality code

```shell
$ >  docker-compose exec web flake8 .
```

### Para dar formato al código

```shell
$ >  docker-compose exec web black . --check
```

### Para ordenar imports

```shell
$ >  docker-compose exec web isort .
```


