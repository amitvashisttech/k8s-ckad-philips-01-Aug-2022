## In case you master or any worker node stuck in a NotReady State: 
## Then follow this procedure 

## Check the Network Pod Status: 

```
kubectl get nodes 
kubectl get pods -n kube-system -o wide 

```

Note Point : In Case you are getting imagepull error stating that you have reached to max limit of downloads, then apply the following solution.

## Excute the following on your master node or from where you can run kubectl & Docker commands 

# Docker login
```
docker login
ls /root/.docker/config.json
```

# Create a Secret in K8s for Docker Registry
```
kubectl create secret generic regcred --from-file=.dockerconfigjson=/root/.docker/config.json --type=kubernetes.io/dockerconfigjson -n kube-system

kubectl get secrets -n kube-system | grep -i regcred
```

# Delete Calico Deployment 
```
kubectl  delete -f calico.yaml
kubectl  get nodes
kubectl  get pods -n kube-system
```



# Apply Calico Deployment 
```
kubectl  apply -f calico.yaml
kubectl  get nodes
kubectl  get pods -n kube-system
```
