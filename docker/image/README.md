# Docker Image Management:
![Docker Image management](https://github.com/ismail-h-rana/essential_docs/blob/main/docker/image/docker-image.png?raw=true)


Build an image from a Dockerfile:
```
docker build -t <image_name>:<tag> -f <dockerfile_path>
```
```
docker build -t <image_name>:<tag> . –no-cache
```

Pull an image from a registry:
```
docker pull <image_name>:<tag>
```
Push an image to a registry:
```
docker push <image_name>:<tag>
```
Create an image from a container:
```
docker commit <container_id> <image_name>:<tag>
```
Tag an image:
```
docker tag <image_name>:<tag> <image_name>:<new_tag>
```
Show all images:
```
docker images
```
Show history of an image:
```
docker history <image_name>:<tag>
```
Remove an image:
```
docker rmi <image_name>:<tag>
```
Save an image:
```
docker save <image_name>:<tag> > <image_name>.tar
```
Load an image:
```
docker load -i <image_name>.tar
```
Remove unused images:
```
docker image prune
```

Remove all images:
```
docker rmi $(docker images -q)
```
