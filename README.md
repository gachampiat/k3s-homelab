Install master :

```
curl -sfL https://get.k3s.io | sh -s - server --disable traefik --datastore-endpoint="https://nas.lan:30001" --datastore-cafile=/usr/share/PKI/etcd/etcd_intermediate_ca.pem --datastore-certfile=/usr/share/PKI/etcd/client.pem --datastore-keyfile=/usr/share/PKI/etcd/client-key.pem
```

Install slave : 

```
curl -sfL https://get.k3s.io | K3S_URL=https://master1.lan:6443 K3S_TOKEN=mynodetoken sh -
```