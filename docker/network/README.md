# Docker Networks:

![Docker Networks](https://github.com/ismail-h-rana/essential_docs/blob/main/docker/network/docker-network.png?raw=true)


Create a network:
```
docker network create <network_name>
```
```
docker network create --driver <driver> <network_name>
```
Connect a container to a network:
```
docker network connect <network_name> <container_name>
```
Disconnect a container from a network:
```
docker network disconnect <network_name> <container_name>
```

Show all networks:
```
docker network ls
```
Show network information:
```
docker network inspect <network_name>
```
Show network statistics:
```
docker network stats <network_name>
```
Remove all networks:
```
docker network prune
```
Remove a network:
```
docker network rm <network_name>
```


