```
  269  kubectl get ns
  270  kubectl create ns myspace  --dry-run -o yaml
  271  kubectl create ns myspace  --dry-run -o yaml > 01-Namespace.yaml
  272  ls
  273  vim 01-Namespace.yaml
  274  ls
  275  kubectl  apply -f 01-Namespace.yaml
  276  kubectl  get ns
  277  kubectl  run hello-k8s --image=nginx --port=80
  278  kubectl  get pods
  279  kubectl get pods --all-namespaces
  280  kubectl  run hello-k8s --image=nginx --port=80
  281  kubectl  run hello-k8s --image=nginx --port=80 -n myspace
  282  kubectl get pods --all-namespaces
  283  kubectl create deploy hello-deployment --help
  284  kubectl create deploy hello-deployment --image=amitvashist7/k8s-tiny-web --port=80 --replicas=3 -n myspace --dry-run -o yaml
  285  kubectl create deploy hello-deployment --image=amitvashist7/k8s-tiny-web --port=80 --replicas=3 -n myspace --dry-run -o yaml > 02-hello-deployment.yaml
  286  ls
  287  vim 02-hello-deployment.yaml
  288  ls
  289  kubectl  apply -f 02-hello-deployment.yaml
  290  kubectl get deploy
  291  kubectl get deploy -n myspace
  292  kubectl get pods --all-namespaces
  293  kubectl  delete -f 01-Namespace.yaml
  294  kubectl get pods --all-namespaces
```
