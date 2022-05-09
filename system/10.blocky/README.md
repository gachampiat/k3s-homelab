# Installation

```
cd mariadb
kubectl apply -f secrets.yaml
helm install mariadb-blocky bitnami/mariadb -n system -f values.yaml

cd ..
kubectl apply -f Certificates.yaml 
helm install blocky k8s-at-home/blocky -n system -f values.yaml
kubectl apply -f IngressRouteHTTP.yaml
kubectl apply -f IngressRouteUDP.yaml

cd prometheus
kubectl apply -f secrets.yaml
kubectl apply -f dc-blocky-metrics.yaml
kubectl apply -f dc-blocky-logs.yaml
```