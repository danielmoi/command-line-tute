# `docker`


## Name
Docker Command Line utility

----
## Usage

```
$ docker [command] [options]
```


----
## Description
Docker is "a self-sufficient runtime for containers"

Docker provides a way to run applications securely isolated in a container, packaged with all its dependencies and libraries.

Website: https://docs.docker.com/


---
## Examples
List containers
```
$ docker ps
```

List images
```
$ docker images
```

Run a command in a running container (in this example, open a bash shell)
```
$ docker exec -it <container-id> bash
```

Remove unused data, including volumes
```
$ docker system prune --volumes -f
```
