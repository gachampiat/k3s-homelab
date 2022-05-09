# Installation : 


```
kubectl apply -f secrets.yaml 
kubectl apply -f certificate.yaml
helm install vaultwarden k8s-at-home/vaultwarden -f values.yaml -n services
```