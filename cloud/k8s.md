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


## General issue

### Kubectl

- Unable to use kubectl
  - The connection to the server localhost:8080 was refused - did you specify the right host or port?
```
<!-- Start the docker and minikube!!!!!! -->
```



## Reference

- [service-monitors](https://observability.thomasriley.co.uk/prometheus/configuring-prometheus/using-service-monitors/)