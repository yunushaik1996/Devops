# Basic Yaml file (Manifest files)
## How to create Name spaces
```bash
kind: Namespace
apiVersion: "v1"
metadata:
 name: nginx
```
## To Excute this yml file use the below command.
```bash
kubectl apply -f filename
```
## Create Pod inside Namespace
```bash
kind: Pod
apiVersion: "v1"
metadata:
  name: nginx-pod
  namespace: nginx
spec:
    containers:
    - name: nginx
      image: nginx:latest
      ports:
       - containerPort: 80
```
## To Excute this yml file use the below command.
```bash
kubectl apply -f filename
```
## To Enter into the Pod 
```bash
 kubectl exec -it nginx-pod -n nginx -- bash
```
## To confrim in bash curl 127.0.0.1

## Describe the pod in the namespace
```bash
kubectl describe pod/podname -n namespace
```
## Deploymet yaml 

```bash
kind: Deployment
apiVersion: apps/v1
metadata:
  name: deploymet-pod
  namespace: nginx
spec:
  replicas: 2
  selector:
    matchLabels:
      apps: nginx
  template:
    metadata:
      labels:
        apps: nginx
    spec:
      containers:
      - name: nginx
        image: nginx:latest
        ports:
        - containerPort: 80
```
## To Excute this yml file use the below command.
```bash
kubectl apply -f filename
```
## To check the Deployment status 

```bash
 kubectl get deployment -n nginx
```
## To scale up the Pods
```bash
 kubectl scale deployment/pod-name -n nginx --replicas=5
 kubectl get deployment -n nginx
 kubectl get pods -n nginx
```

