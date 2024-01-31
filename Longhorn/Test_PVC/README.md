# Longhorn

# Create PVC:
```bash
kubectl apply -f Longhorn/Test_PVC/01-PVC.yaml
```

# Create deployment:
```bash
kubectl apply -f Longhorn/Test_PVC/02-MyGifService-Deployment-PVC.yaml
```

# Detach volume:
```bash
kubectl scale deployment mygifservice-deployment -n volumes-sample \
    --replicas=0
```

# Attach volume:
```bash
kubectl scale deployment mygifservice-deployment -n volumes-sample \
    --replicas=1
```