# Docker

## What's Docker 


## Difference between VM

![](/src/DockervsVM.png)

## How to install the docker

### Ubuntu

**Docker installation on ubuntu**
```bash=
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu `lsb_release -cs` test"
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

### MacOS

- [How to install docker on mac system](https://docs.docker.com/desktop/install/mac-install/)

## Command

### image

- Build image
```docker=
docker build [OPTIONS] .
```

**[OPTIONS]**
```shell=
-t [Tag]
```
- Push image
```docker=
docker push [user_name]/[image_name]
```

- Delete dangling images
```shell=
docker image prune
```

- Delete unused images
```shell=
docker image prune -a
```

### Container

```shell=
docker ps [OPTIONS]
```
**[OPTIONS]**
```shell=
-a [ALL]
```

- Stop all running container 
```
docker container stop $(docker ps -q)
```

- Remove all stop container
```
docker container prune
```

### System prune

```
docker system prune
```

- all stopped containers
- all networks not used by at least one container
- all volumes not used by at least one container
- all images without at least one container associated to them
- while clearing all build caches


## Mulitple Stage Build

### Example

**Python requirement multiple stage building**

```=docker
# Build stage
From python:3.9-slim AS build

RUN pip install --upgrade pip
RUN python3 -m pip install -U pip
RUN pip install --upgrade setuptools

RUN python -m venv /opt/venv
ENV PATH="/opt/venv/bin:$PATH"
COPY requirements.txt .
RUN pip install -r ./requirements.txt

# Production stage
From python:3.9-slim AS production

# copy the python build lib from build container
COPY --from=build /opt/venv /opt/venv
ENV PATH="/opt/venv/bin:$PATH"
# Set up the run path for python 
ENV PYTHONPATH=/app
```

## Docker Compose

```
docker-compose up [OPTIONS]
[OPTIONS]
-d deamon mode
--build build container instead of using existing one 
```


```
docker-compose down
```

### Similar Topic

- [Kubernetes](/cloud/k8s.md)


## Reference

- [docker-turtorial Github](https://github.com/twtrubiks/docker-tutorial)
- [docker-command-line](https://pjchender.dev/devops/docker-command-line/)