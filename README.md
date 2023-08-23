# Django-Todo-with-Nginx-K8s


This repository contains Kubernetes configuration files to deploy a Django-based todo application using Docker containers and Kubernetes.

## Prerequisites

Before you begin, ensure you have the following prerequisites:

- Docker installed (for building container images)
- Minikube (or another Kubernetes environment) set up
- kubectl CLI tool installed

## Deployment

Follow these steps to deploy the Django todo application on Kubernetes:

1. Build Docker Images:

   ```bash
   docker build -t psharma10394/djangoapplication:latest -f Dockerfile .

Apply Kubernetes Configuration:


kubectl apply -f pod.yml

Once the deployment is successful, you can access the application using the following steps:

Get the Minikube IP:
kubectl get pod --namespace=django-todo-app -o wide


Access the Django application:

Open a web browser and go to http://<minikube-ip>:8001 to access the Django todo app.


kubectl delete -f pod.yml



