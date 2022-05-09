```
kubectl apply -f secrets.yaml
helm install --values values.yaml -n system csi-api-nfs democratic-csi/democratic-csi
```