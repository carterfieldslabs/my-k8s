# Create Dynamic Provision NFS Persistent Volumes

## Install on each client node

sudo apt install -y nfs-common

# Setup Storage Node

kubectl create -f rbac.yaml -f class.yaml -f deployment.yaml
