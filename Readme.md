## Tested on the following
kind version 0.11.1
kubectl v1.22.2
kubernetes v1.21.2
cilium v1.11.4

### Create the cluster
kind create cluster --config config.yaml

### Apply cilium CNI
kubectl apply -f manifests/cilium-cni.yaml
```
➜  nynog-k8s-networking-101 kubectl apply -f manifests/cilium-cni.yaml
serviceaccount/cilium created
serviceaccount/cilium-operator created
configmap/cilium-config created
clusterrole.rbac.authorization.k8s.io/cilium created
clusterrole.rbac.authorization.k8s.io/cilium-operator created
clusterrolebinding.rbac.authorization.k8s.io/cilium created
clusterrolebinding.rbac.authorization.k8s.io/cilium-operator created
daemonset.apps/cilium created
deployment.apps/cilium-operator created
```

### Delete the cluster
kind delete cluster --name nynog-k8s-networking-101