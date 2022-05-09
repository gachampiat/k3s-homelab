
# Install

```
k apply -f Certificates.yaml -f grafana-datasources.yaml -f secrets.yaml
helm install -f values.yaml kube-prometheus-stack prometheus-community/kube-prometheus-stack -n system
```

## Prometheus metrics configuration

Add to master nodes : 

```
root@master1:/home/ubuntu# cat /etc/rancher/k3s/config.yaml
kube-controller-manager-arg:
- "bind-address=0.0.0.0"
kube-proxy-arg:
- "metrics-bind-address=0.0.0.0"
kube-scheduler-arg:
- "bind-address=0.0.0.0"


root@master1:/home/ubuntu# systemctl restart k3s
```

Add to worker nodes : 

```
root@slave1:/home/ubuntu# mkdir /etc/rancher/k3s/
root@slave1:/home/ubuntu# cat /etc/rancher/k3s/config.yaml
kube-proxy-arg:
- "metrics-bind-address=0.0.0.0"

root@slave1:/home/ubuntu# systemctl restart k3s-agent
```


# Ref :

https://github.com/k3s-io/k3s/issues/3619