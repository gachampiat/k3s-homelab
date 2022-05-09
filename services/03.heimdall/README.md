# Installation 

```
kubectl apply -f certificate.yaml
helm install heimdall k8s-at-home/heimdall -f values.yaml -n services
```