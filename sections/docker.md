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