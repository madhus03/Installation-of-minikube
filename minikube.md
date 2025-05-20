# HOW TO INSTALL MINIKUBE ON YOUR LOCAL LAPTOP

1. Install Minikube
2. Install Kubectl

To install Minikube, first you need a docker environment or a virtual machine on your laptop. On top of your docker/virtual machine environment we will install minikube cluster.

You can have vm of your choice - Oracle virtual box, VMware workstation, etc.
Make sure it's compatible on your host.

Your host must have :

- 2 CPUs or more
- 2GB of free memory
- 20GB of free disk space
- Internet connection

## 1. Installation

Choose your target platform (Linux, Windows, or Mac)

I have chose Linux.

![image](https://github.com/user-attachments/assets/c5255c32-7a48-4f03-bbd1-aece9cdf3a63)

run the below command on your terminal

```bash
curl -LO https://github.com/kubernetes/minikube/releases/latest/download/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube && rm minikube-linux-amd64
```

## 2. Starting your cluster
From a terminal with administrator access (but not logged in as root), run:

```bash
minikube start
```
If minikube fails to start, try setting up a compatible container or virtual-machine manager.

## 3.Cluster Interaction

you can start to use the minikube by running this command 

```bash
kubectl get po -A
```

## 4. Deploying the applications

To Create a sample deployment

```bash
kubectl create deployment hello-minikube
```

To create a sample service

```bash
kubectl create service hello-minikube
```
