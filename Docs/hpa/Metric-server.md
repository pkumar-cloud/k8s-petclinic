# Metric server is required for Horizontal Pod Autoscaler

## What is Metric Server?
```sh
It collects metrics like CPU, memory or Disk IO consumption for containers or nodes, from the Summary API, exposed by Kubelet on each node.
```

## Enable 4443 port on Master and Worker Nodes
```sh
4443
```
## Installation via components.yaml manifest
```sh
#Source -> https://github.com/kubernetes-sigs/metrics-server
kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/components.yaml
```

## Installation via local copy
```sh
git clone https://github.com/kubernetes-sigs/metrics-server.git
#git clone https://github.com/prawinkorvi/metric-server.git
kubectl create -f .
```

## HELM way
```sh
#Source -> https://artifacthub.io/packages/helm/metrics-server/metrics-server
#Add the metrics-server repo to helm:
helm repo add metrics-server https://kubernetes-sigs.github.io/metrics-server/
helm upgrade --install metrics-server metrics-server/metrics-server
```
## Test
```sh
kubectl top pods
kubectl top nodes
```

