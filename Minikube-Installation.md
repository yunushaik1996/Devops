# Mini Kube Installation for Ubuntu.

## 1. Update System Packages.
```bash
sudo apt update
```
## 2. Install some basic required packages.
```bash
sudo apt install -y curl wget apt-transport-https
```
## 3. Install Docker.
```bash
sudo apt install -y docker.io
```
## Start and enable Docker.
```bash
sudo systemctl enable --now docker
```
## Add current user to docker group.
```bash
sudo usermod -aG docker $USER && newgrp docker
```
## Now, logout (use exit command) and connect again.
# 4. Install Minikube
Download the Minikube binary using curl:
```bash
curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
```
## Make it executable and move it into your path:
```bash
chmod +x minikube
sudo mv minikube /usr/local/bin/
```
## 5. Install kubectl
Download kubectl, which is a Kubernetes command-line tool.
```bash
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
```
## Make it executable and move it into your path:
```bash
chmod +x kubectl
sudo mv kubectl /usr/local/bin/
```
## Start Minikube
Now, you can start Minikube with the following command:
```bash
minikube start --driver=docker --vm=true
```
This command will start a single-node Kubernetes cluster inside a Docker container.

## Check Cluster Status
```bash
minikube status
```
```bash
kubectl get nodes
```
## Stop Minikube
When you are done, you can stop the Minikube cluster with:

```bash
minikube stop
```
## Delete Minikube Cluster
```bash
Delete Minikube Cluster
```

That's it! You've successfully installed Minikube on Ubuntu.

# Mini kube for local

Open Power shell
```bash
cd $env:USERPROFILE\Downloads
```
## 1. Install Docker
Download Docker Desktop
```bash
https://www.docker.com/products/docker-desktop/
```
Install and start Desktop Docker

Verify:
```bash
docker --version
```
## 2. Install kubectl
Open Power shell
```bash
curl.exe -LO https://dl.k8s.io/release/v1.30.0/bin/windows/amd64/kubectl.exe
kubectl version --client
```
## 3. Install Minikube
```bash
curl.exe -LO https://storage.googleapis.com/minikube/releases/latest/minikube-windows-amd64.exe
```
## 4. Rename the file 
```bash
Rename-Item minikube-windows-amd64.exe minikube.exe
```
## 5. Create Directory
```bash
dir minikube*.exe
```
```bash
New-Item -ItemType Directory -Path "C:\Program Files\minikube" -Force
```
## 6. Move minikube.exe
```bash
Move-Item minikube.exe "C:\Program Files\minikube\"
```
## 7. Check the Version
```bash
minikube version
```
## 8. Start Kubectl 
```bash
minikube start --driver=docker
kubectl get nodes
```
<img width="946" height="423" alt="image" src="https://github.com/user-attachments/assets/04f79f0c-d0c5-4916-b181-f47cab2664e9" />


That's it! You've successfully installed Minikube in local.








