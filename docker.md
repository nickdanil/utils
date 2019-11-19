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
docker run -d -p 8000:8000 -p 9000:9000 -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer
```

## ELK
```
TODO
```

## RabbitMQ Management
```
$ docker run -d --hostname rabbit --name rabbit --restart always -p 15672:15672 rabbitmq:3-management
```

## Postgres
```
TODO
```

## Postgres + pgadmin
```
TODO
```