# NODE JS - POSTGRES

## Run Postgres Container

```docker
  $ docker-compose up -d postgres
```

### Check State

```docker
$ docker-compose ps
```

### Down Docker

```docker
  $ docker-compose down
```

### Explore DB

```docker
  $ docker-compose exec postgres bash
    /# psql -h localhost -d postgres -U postgres
      postgres=# \d+
```

## Connect PGADMIN

```docker
  $ docker-compose up -d pgadmin
```

### Get IP

```docker
  $ docker ps
  $ docker inspect [postgres_container_id]
```

### Create Tasks Table

```sql
  CREATE TABLE tasks (
	id serial PRIMARY KEY,
	title VARCHAR (255) NOT NULL,
	completed boolean DEFAULT false
  );
```

## Connect Node-Postgres
```
  $ npm install pg
```