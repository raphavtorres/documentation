# Docker Config

## Docker commands

## Remove everything
```pws
docker system prune --all --force --volumes
```

### Docker build 

Create image
```pws
docker build -t <name>:<tag> .
```


### Docker image (Work with your images)
List images
```pws
docker images
```

Compress image
```psw
docker image save -o <archive_name>.tar <imagen_ame>:<version>
```

Unzip image
```pws
docker image load -i <archive_name>.tar
```

Remove image
```pws
docker image rm <image_id>
```

        
### Docker run (create and run container)
-it: run in interactive mode

-d: run in background

-p: specify the port it is running on

--name: specify the container name

-e: specify environment variables

Example:
```pws
docker run -d --name <container_name> -p <host_port>:<docker_port> <image_name>:<version>
```


### Docker exec (execute command in container)
```pws
docker exec <contaniner_name> <command>
```
        
### Docker stop/start (stop and start container)
```pws
docker stop <container_name>
docker run <container_name> 
```
### Remove Container
force to stop and remove
```pws
-f
```
```pws
docker rm <container_name>
```


### Docker volume
```pws
docker volume create <volume_name>
docker run -it -v <volume_name>:/<directory_name> <image>
```

### Docker copy files
```pws
docker cp <origin> <destiny>
```


### Docker network
```pws        
docker network ls
docker network create --driver bridge <name>
```

Run specific network
```pws
--network <network>
```


### My shortcuts
```pws
alias docker-stop='docker stop $(docker ps -a -q)'

alias docker-psrm='docker rm $(docker ps -a -q)'

alias docker-imgrm='docker rmi $(docker images -q)'

alias docker-vlrm='docker volume rm $(docker volume ls -q)'

alias docker-ntrm='docker network rm $(docker network ls -q)'
```

         
# DOCKERFILE
FROM: image (Linux, Ubuntu), platform (python, nodejs)

WORKDIR: work directory (executes the commands inside this directory)

COPY: copy your local directory and add in image

ADD: Copies an internet file or adds and unzips a local file and adds an image

RUN: Commands to install the dependencies in the image construction

ENV: environment configurations

EXPOSE: expose your application to a determined port

USER: user who will execute the application

CMD: commands to run the application (runs afeter the image construction)
