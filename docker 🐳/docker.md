# Docker Config

## Docker commands
    
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
docker image save -o <archiveName>.tar <imagename>:<version> -> comprimir sua imagem
```

Unzip image
```pws
docker image load -i <archiveName>.tar -> descompactar a imagem
```

Remove image
```pws
docker image rm <imageId> -> remover uma imagem
```
        
### Docker run (create and run container)
-it -> rodar no modo interativo
-d -> rodar em background
-p -> especificar a porta que está rodando
--name -> especificar o nome do container

Example:
```pws
docker run -d --name <containerName> -p <hostPort><dockerPort> <imageName>:<version>
```

### Docker exec (execute command in container)
```pws
docker exec <contaninerName> <command>
```
        
### Docker stop/start (stop and start container)
```pws
docker stop <containerName>
docker run <containerName> 
```
### Remove Container
force to stop and remove
```pws
-f
```
```pws
docker rm <containerName>
```


### Docker volume
```pws
docker volume create <volumeName>
docker run -it -v <volumeName>:/<directoryName> <image>
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
         
# DOCKERFILE - 
FROM -> image (Linux, Ubuntu), platform (python, nodejs)

WORKDIR -> work directory (executes the commands inside this directory)

COPY -> copy your local directory and add in image

ADD -> Copies an internet file or adds and unzips a local file and adds an image

RUN -> Commands to install the dependencies in the image construction

ENV -> environment configurations

EXPOSE -> expose your application to a determined port

USER -> user who will execute the application

CMD -> commands to run the application (runs afeter the image construction)
