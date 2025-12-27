# Mini Kube Installation for Ubuntu.

# 1. Update System Packages.
```bash
sudo apt update
```
# 2. Install some basic required packages.
```bash
sudo apt install -y curl wget apt-transport-https
```
# 3. Install Docker.
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
# 5. Install kubectl
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

hat's it! You've successfully installed Minikube on Ubuntu.






