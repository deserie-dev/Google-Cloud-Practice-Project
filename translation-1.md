# LAB: Google Cloud Fundamentals: Getting Started With Kubernetes Engine

## Objectives:

In this lab you will elarn how to perform the following tasks: 

* Provision a Kubernetes cluster using Kubernetes Engine
* Deploy and manage Docker containers using kubectl

## Steps:

1. List the APIs and services available to you in your current project.
```
gcloud services list --available
```
2. List enabled services.
```
gcloud services list
```
3. Place your zone into an environment variable
```
export MY_ZONE=
```
4. Start a Kubernetes cluster managed by Kubernetes Engine and configure it to run two nodes.
```
gcloud container clusters create cluster-name --zone $MY_ZONE --num-nodes 2
```
5. After the cluster is created, check your installed version of Kubernetes.
```
kubectl version
```
6. To run and deploy a container, launch a single instance of the nginx container.
```
kubectl create deploy nginx --image=nginx:1.17.10
```
7. View the pod running the nginx container.
```
kubectl get pods
```
8. Expose the nginx container to the Internet.
```
kubectl expose deployment nginx --port 80 --type LoadBalancer
```
9. View the new service.
```
kubectl get services
```
10. Scale up the number of pods running on your service.
```
kubectl scale deployment nginx --replicas 3
```
11. Confirm that Kubernetes has updated the number of pods.
```
kubectl get pods
```
12. Confirm that your external IP address has not changed.
```
kubectl get services
```