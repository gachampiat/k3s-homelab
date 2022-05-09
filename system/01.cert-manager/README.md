```
helm install cert-manager jetstack/cert-manager   --namespace cert-manager   --create-namespace   --version v1.7.0  --set installCRDs=true
kubectl apply -f secrets.yaml
kubectl apply -f ClusterIssuer.yaml
```