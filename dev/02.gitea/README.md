# Installation 

```
kubectl apply -f configMaps.yaml
kubectl apply -f secrets.yaml
kubectl apply -f certificate.yaml
helm install gitea gitea-charts/gitea -f values.yaml -n dev
```