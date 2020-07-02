# Docker

#### Dockerfile example
```docker
FROM ubuntu:latest

COPY source target
RUN echo
```

#### Build image
```console
foo@bar:~$ docker build -t image-name folder-with-dockerfile
```

#### Create container from image
```console
foo@bar:~$ docker create -ti --name container-name image-name
```

#### Create container from image with volume
```console
foo@bar:~$ docker create -ti -v $PWD:/home/folder-name --name container-name image-name
```

#### Detach container
```
Ctrl-p + Ctrl-q
```