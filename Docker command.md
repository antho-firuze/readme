# Docker Command

## Execute docker compose

```bash
docker compose up -d --remove-orphans --build
```

```bash
docker compose up -d --build
```

```bash
docker compose up -d
```

```bash
docker compose down
```

## Show docker log

```bash
docker ps
```

```bash
docker logs -f [container_name/container_id]
```

## Enter into the container

```docker exec -ti [container_name/container_id] sh```  
```docker exec -ti [container_name/container_id] /bin/bash```  
```docker exec -ti [container_name/container_id] /bin/bash```

## Execute command without enter into the container

```docker exec [container_name/container_id] php start.php status```
```docker exec [container_name/container_id] npm install axios --save```
```docker exec [container_name/container_id] npm dev```

## Running docker and then execute the command

```docker run -it redis redis-cli -h 127.0.0.1```

## Show all docker container

```docker images```
```docker image rm image_name```

## Show running docker container

```docker ps```

## Remove docker container

```docker rm [containerid containerid ...]```

## +++ REMOVE ALL IMAGE +++

```docker rm -vf $(sudo docker ps -aq)```
