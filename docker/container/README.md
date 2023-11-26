# Docker Container Management:

- [Container Management](#container-management)
- [Running a Container](#running-a-container)


## Container Management

![Docker Container management](https://github.com/ismail-h-rana/essential_docs/blob/main/docker/container/docker-container.png?raw=true)

Learn how to create, manage, run, stop, and remove containers from your Docker environment:

Create a container:
```
docker create -it --name <container_name> <image_name>:<tag>
```
Start a container:
```
docker start <container_name>
```
Stop a container:
```
docker stop <container_name>
```
Remove a container:
```
docker rm <container_name>
```
Remove all containers:
```
docker rm $(docker ps -a -q)
```
Remove running container:
```
docker rm -f <container_name>
```
Show all containers:
```
docker ps -a
```
View logs for a container:
```
docker logs <container_name>
```
View logs for all containers:
```
docker logs -f $(docker ps -a -q)
```
View details for a container:
```
docker inspect <container_name>
```
View stats for a container:
```
docker stats <container_name>
```
Retrieve the IP address of a container:
```
docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' <container_name>
```
Copy files from one container to another:
```
docker cp <container_name>:<source_path> <destination_path>
```
Rename a container:
```
docker rename <old_container_name> <new_container_name>
```
Retrieve logs created before a specific date:
```
docker logs --since <date>
```
Retrieve logs created after a specific date:
```
docker logs --until <date>
```
View history of a container:
```
docker history <container_name>
```
View image used by a container:
```
docker inspect --format='{{.Image}}' <container_name>
```
View networks used by a container:
```
docker inspect --format='{{json .NetworkSettings.Networks}}' <container_name>
```
View ports used by a container:
```
docker inspect --format='{{json .NetworkSettings.Ports}}' <container_name>
```
View volumes used by a container:
```
docker inspect --format='{{json .Volumes}}' <container_name>
```
View environment variables used by a container:
```
docker inspect --format='{{json .Config.Env}}' <container_name>
```
View real-time events for a container:
```
docker events <container_name>
```
View real-time events for all containers:
```
docker events -f
```
View port mappings for a container:
```
docker port <container_name>
```
View running processes in a container:
```
docker top <container_name>
```
View live resource usage statistics for a container:
```
docker stats --no-stream <container_name>
```
View changes to files or directories in a container:
```
docker diff <container_name>
```
View status of a container:
```
docker inspect --format='{{.State.Status}}' <container_name>
```
View health status of a container:
```
docker inspect --format='{{.State.Health.Status}}' <container_name>
```
Update the configuration of a container:
```
docker update <container_name>
```
Copy a local file to a container:
```
docker cp <local_file_path> <container_name>:<destination_path>
```
Copy a container to a local file:
```
docker cp <container_name>:<source_path> <local_file_path>
```

## Running a Container


![Docker Running Container](https://github.com/ismail-h-rana/essential_docs/blob/main/docker/container/docker-container-run.png?raw=true)


Create and Run a container from an image:
```
docker run -it --name <container_name> <image_name>:<tag>
```
Establish a conncetion with a container by mapping host ports to container ports:
```
docker run -it --name <container_name> -p <host_port>:<container_port> <image_name>:<tag>
```
Run a container and remove it after it stops:
```
docker run -it --rm --name <container_name> <image_name>:<tag>
```
Start a container:
```
docker start <container_name>
```
Stop a container:
```
docker stop <container_name>
```
Remove a container:
```
Remove running container:
```
docker rm -f <container_name>
```
Restart a container:
```
docker restart <container_name>
```
Pause a container:
```
docker pause <container_name>
```
Unpause a container:
```
docker unpause <container_name>
```
Kill a container:
```
docker kill <container_name>
```
View details for a container:
```
docker inspect <container_name>
```
Attach local standard input output and error streams to a container:
```
docker attach <container_name>
```
Attach local standard input to a running container:
```
docker attach -i <container_name>
```
Run a shell inside a running container:
```
docker exec -it <container_name> bash
```
