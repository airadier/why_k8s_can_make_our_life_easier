# Install Kubernetes with Vagrant (Ubuntu host OS)

## Requirements

- vagrant (>2.0) with scp and hostmanager plugins installed
- 4GB memory available
- Virtual box
- kubectl installed (1.8)

## Instructions

- Provision and start the cluster
```
vagrant up
```

- Get kubeconfig
```
vagrant scp master:/etc/kubernetes/admin.conf ./kubeconfig
```

- Check if it works
```
kubectl get po --kubeconfg ./kubeconfig
```
