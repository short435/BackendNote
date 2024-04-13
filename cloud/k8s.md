# Kubernetes


## What's Kubernetes?

Kubernetes are able to deploy, scale and manage the containers.

- Deploying on mupilte machines.
- Scaling for loadbalance.
- Detecting the errors and relaunching services.

## Main Object for Kubernetes

### Pod

The smallest unit in k8s. A pod would be assisgned to a application. Such as Nginx/Api/etc...

There could be mulipile continer in a pod. However it would be great to have only one container in one pod.

### Worker Node

#### kube-apiserver

#### etcd

#### kube-scheduler

#### kube-controller-manager


### Master Node

### Cluster

A Cluster should be a set for Nodes and Pods.



## How to Set up the k8s on local machine

### Mac OS

#### Minikube (with Docker Desktop)

**Installation**

- Installtion
```shell=
brew install minikube
```
**Launch the minikube**

- Launch the minikube
```shell=
minikube start
```

- Launch with mounting the local path to the VM
```shell=
minikube start --mount --mount-string={Mount Path}
```

- Launch with assigning specific memeory for the VM
```shell=
minikube start --memory 5048
```
==It may encounter the memory for the docker desktop are lower than your reqired. Please set up the memeory usage in docker desktop.==


- Stop
```shell
minikube stop
```

- Delete
```shell
minikube delete
```

- Check current survices
```shell
minikube service list
```

- Link the port of the service with local machine
```shell
minikube service []
```

#### Kubectl

Command line tool for K8S.

- Check if the Kubectl are already installed on your machine.
```shell=
kubectl version --client
```

**Installtion**
```shell=
brew install kubectl
```

```

```


## General issue

### Kubectl

- Unable to use kubectl
  - The connection to the server localhost:8080 was refused - did you specify the right host or port?
```
<!-- Start the docker and minikube!!!!!! -->
```



## Reference

- [service-monitors](https://observability.thomasriley.co.uk/prometheus/configuring-prometheus/using-service-monitors/)
