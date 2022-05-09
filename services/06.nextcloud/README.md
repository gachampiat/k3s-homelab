# Installation : 


```
cd mariadb
kubectl apply -f secrets.yaml
helm install mariadb-nextcloud bitnami/mariadb -n services -f values.yaml

cd ..
kubectl apply -f certificate.yaml
kubectl apply -f secrets.yaml
helm install -f values.yaml nextcloud nextcloud/nextcloud -n services
```