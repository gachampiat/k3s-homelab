Installation : 

```
helm install traefik traefik/traefik -f values.yaml -n system
```


Upgrade :

```
helm upgrade --reuse-values -f values.yaml -n system traefik traefik/traefik
```

Uninstall : 

```
helm uninstall traefik -n system
```