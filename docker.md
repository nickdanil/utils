# Docker command snippets

## PORTAINER
```
$ docker volume create portainer_data
```

### PORTAINER - WINDOWS
```
$ docker run -d -p 8000:8000 -p 9000:9000 --name portainer --restart always -v \\.\pipe\docker_engine:\\.\pipe\docker_engine -v portainer_data:C:\data portainer/portainer
```

### PORTAINER - LINUX
```
docker run -d -p 8000:8000 -p 9000:9000 --name portainer --restart always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer
```

## ELK
UBUNTU
```
$ sudo sysctl -w vm.max_map_count=262144
$ sudo docker run --restart=always -p 5601:5601 -p 9200:9200 -p 5044:5044 -e MAX_MAP_COUNT=262144 -it --name elk sebp/elk 
```

## RabbitMQ Management
```
$ docker run -d --hostname rabbit --name rabbit --restart always -p 15672:15672 rabbitmq:3-management
```

## Postgres
```
$ docker volume create postgres_data
$ docker run -d --name postgres -e 'POSTGRES_PASSWORD=postgres' -v postgres_data:/var/lib/postgresql/data -p 5432:5432 postgres -c shared_preload_libraries='pg_stat_statements' -c pg_stat_statements.max=10000 -c pg_stat_statements.track=all
```

## Pgadmin
```
$ docker volume create pgadmin4_data
$ docker run -p 8080:80 -e 'PGADMIN_DEFAULT_EMAIL=admin@pgadmin4.com' -e 'PGADMIN_DEFAULT_PASSWORD=admin' -v pgadmin4_data:/var/lib/pgadmin -d dpage/pgadmin4
```
