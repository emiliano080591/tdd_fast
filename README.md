# FastApi example

Ejemplo de un api con FastApi, docker y CI

# Test-Driven Development with FastAPI and Docker

![Continuous Integration and Delivery](https://github.com/emiliano080591/tdd_fast/workflows/Continuous%20Integration%20and%20Delivery/badge.svg?branch=main)

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

### Generar imagen Docker para integracion continua

```shell
$ >  docker build -f Dockerfile.prod -t docker.pkg.github.com/<Usuario>/<Nombre_proyecto_en_github>/summarizer:latest ./
```

### Loguearse en github para subir imagen docker

```shell
$ >  docker login docker.pkg.github.com -u <USERNAME> -p <TOKEN>
```

### Hacer push de la imagen Docker

```shell
$ >  docker push docker.pkg.github.com/<USERNAME>/<REPOSITORY_NAME>/summarizer:latest
```

### Para ver la imagen generada

https://github.com/<USERNAME>/<REPOSITORY_NAME>/packages



