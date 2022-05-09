# Installation :


```
kubectl apply -f secrets.yaml
helm install -n system -f values.yaml velero vmware-tanzu/velero
```