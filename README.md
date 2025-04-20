### Instructions to start this app
```bash
minikube start --driver=docker
```

```bash
helm repo add kvaps https://kvaps.github.io/charts
```

```bash
helm repo update
```

```bash
helm install nfs-server kvaps/nfs-server-provisioner --set persistence.enabled=true --set persistence.size=1Gi --set storageClass.name=nfs-sc --set storageClass.defaultClass=false
```

```bash
kubectl apply -R -f .
```

```bash
minikube service nginx-service
```

