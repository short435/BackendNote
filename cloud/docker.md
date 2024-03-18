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

### List container

```shell=
docker ps [OPTIONS]
```
[OPTIONS]
```shell=
-a [ALL]
```

### Pull image

### Delete image

Delete dangling images
```shell=
docker image prune
```

Delete unused images
```shell=
docker image prune -a
```

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



### Similar Topic

- [Kubernetes](/cloud/k8s.md)