# Docker basics notes

## Docker command line documentation
https://docs.docker.com/engine/reference/commandline/cli/


## List of frequent commands and headups

```
docker run image-name
docker ps
docker ps -a (shows just running)

```
If exited=0 -> result is ok
if exited=2 es -> there are errors.

If name is not provided: it's randomly assigned.


## Identify an image
name:tags

## Shows downladed images
```
docker image ls  
docker image
```

When using an image always provide a tag for identify the version, do not rely on _latest_ tag. (It can change and break your app).

## Check logs synchronized
```
docker logs name -f 
```

## Remove a container you no longer need
```
docker rm name
```

You can use just a part of the id to identify the docker 
```
docker stop id
```

Docker Hub limits the number of Docker image downloads (“pulls”) based on the account type of the user pulling the image. There is a command to check it.

## Docker daemon

Docker engine.

The Docker daemon ( dockerd ) listens for Docker API requests and manages Docker objects such as images, containers, networks, and volumes. A daemon can also communicate with other daemons to manage Docker services.

Root permissions. 


## Docker run example

 docker run 
 --rm (Will be deleted when finished)
 -it (interactive mode)
  -v "${PWD}":/srv/jekyll \
 -p 4000:4000 
 jekyll/jekyll:4.2.0 jekyll serve