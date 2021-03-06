# Docker

1. List images

```
$ docker images
############################
sudo docker images --all
REPOSITORY                 TAG                 IMAGE ID            CREATED             SIZE
hello-world                latest              05a3bd381fc2        10 hours ago        1.84kB
dzwicker/docker-youtrack   latest              96df251c60a4        4 weeks ago         892MB
```

2. Delete images by IMAGE_ID

```
sudo docker rmi --force 96df251c60a4
Untagged: dzwicker/docker-youtrack:latest
Untagged: dzwicker/docker-youtrack@sha256:03c1113c6b1ec9bfb17
Deleted: sha256:96df251c60a4ae934f60bff3159c5a198fe9a3fa91da31f51026a0426cf82b46
```

3. Delete all

```
# Delete all containers
docker rm $(docker ps -a -q)
# Delete all images
docker rmi $(docker images -q)
```

4. Connect to container

```
sudo docker exec -it youtrack sh
```
