# Installation


```
kubectl apply -f cm-ca-certificate.yaml
helm install -f values.yaml loki grafana/loki -n system
kubectl apply -f prometheus/configMap.yaml
```