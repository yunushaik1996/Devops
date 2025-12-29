# Basic Yaml file (Manifest files)
## How to create Name spaces
```bash
kind: Namespace
apiVersion: "v1"
metadata:
 name: nginx
```
To excute this yml file use the below command.
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
To excute this yml file use the below command.
```bash
kubectl apply -f filename
```
