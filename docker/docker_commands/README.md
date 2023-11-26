# Docker Commands:
![Docker Commands](https://github.com/ismail-h-rana/essential_docs/blob/main/docker/docker_commands/docker-commands.png?raw=true)

Display docker information:
```
docker info
```
Show docker version:
```
docker version
```
Show docker system information:
```
docker system info
```
Show docker environment information:
```
docker env
```
Show docker statistics:
```
docker stats
```
Show docker events:
```
docker events
```
Show docker logs:
```
docker logs
```
Remove unused images, containers, and networks:
```
docker system prune
```
Remove all images:
```
docker rmi $(docker images -q)
```
Remove all containers:
```
docker rm $(docker ps -a -q)
```
Remove all volumes:
```
docker volume rm $(docker volume ls -q)
```
Remove all networks:
```
docker network rm $(docker network ls -q)
```

List all docker images:
```
docker images
```
List all docker containers:
```
docker ps
```
List all docker volumes:
```
docker volume ls
```
List all docker networks:
```
docker network ls
```
Log in to a docker registry:
```
docker login
```
Log out of a docker registry:
```
docker logout
```
