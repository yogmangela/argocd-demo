What is kompose.io 
it's a tool which helps you to write docker-compose.yaml into kubernetes equavalant .yml files.

- install kompose: got to https://kompose.io/ for intallation and usage
- How to use :
    once you have docker-compose.yml you can run:
```
user@machine dock-compose-to-k8s % kompose convert
INFO Kubernetes file "frontend-service.yaml" created 
INFO Kubernetes file "redis-master-service.yaml" created 
INFO Kubernetes file "redis-slave-service.yaml" created 
INFO Kubernetes file "frontend-deployment.yaml" created 
INFO Kubernetes file "redis-master-deployment.yaml" created 
INFO Kubernetes file "redis-slave-deployment.yaml" created 
```
to conver all the file to k8s .yml.

- then you can 
```
kubectl apply -f frontend-service.yaml,redis-master-service.yaml,redis-slave-service.yaml,frontend-deployment.yaml,redis-master-deployment.yaml,redis-slave-deployment.yaml
```

