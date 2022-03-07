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

