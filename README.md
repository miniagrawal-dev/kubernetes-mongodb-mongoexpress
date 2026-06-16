# Kubernetes MongoDB + Mongo Express Project

## Overview

This project demonstrates deployment of MongoDB and Mongo Express on Kubernetes using:

- Deployments
- Services
- ConfigMaps
- Secrets
- Minikube

## Architecture

Browser
↓
Mongo Express Service
↓
Mongo Express Pod
↓
MongoDB Service
↓
MongoDB Pod

## Components

### MongoDB
- Deployment
- ClusterIP Service
- Credentials stored in Secret

### Mongo Express
- Deployment
- LoadBalancer Service
- Configuration from ConfigMap

## Commands

kubectl apply -f manifests/

kubectl get pods

kubectl get svc

minikube service mongo-express-service

## Learning Outcomes

- Kubernetes Pods
- Deployments
- Services
- ConfigMaps
- Secrets
- Service Discovery

## Architecture
+----------------+
|    Browser     |
+----------------+
|
v
+----------------------+
| Mongo Express Service|
+----------------------+
|
v
+----------------------+
| Mongo Express Pod    |
+----------------------+
|
v
+----------------------+
| MongoDB Service      |
+----------------------+
|
v
+----------------------+
| MongoDB Pod          |
+----------------------+

kubectl apply -f mongo-secret.yaml
kubectl get secret

kubectl apply -f mongo.yaml
kubectl get all

kubectl get pod --watch

kubectl get all | grep mongodb

kubectl apply -f mongo-configmap.yaml
configmap/mongodb-configmap created
kubectl apply -f mongo-express.yaml
kubectl get pod
kubectl get logs mongo-express-cfff

kubectl get service
external ip not assigned yet

minikube service mongo-express-service

username - admin
pass - pass