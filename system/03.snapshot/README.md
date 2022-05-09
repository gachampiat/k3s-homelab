First install Snapshot CRDs : 

```
kubectl kustomize crd | kubectl create -f - 
```

Then install the snapshot controller : 

```
kubectl kustomize snapshot-controller | kubectl create -f - 
```

Then insall the Volume Snapshot Class
```
kubectl apply -f VolumeSnapshotClass.yaml
```