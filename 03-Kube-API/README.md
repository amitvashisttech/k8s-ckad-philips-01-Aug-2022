```
364  kubectl get pods -n kube-system
  365  cd  /etc/kubernetes/manifests/
  366  ls
  367  vim kube-apiserver.yaml
  368  kubectl cluster-info
  369  kubectl version
  370  kubectl api-versions
  371  kubectl api-resources
  372  curl -k https://172.31.0.100:6443
  373  kubectl proxy --address='172.31.0.100' --port=8080 --accept-hosts='.' --accept-paths='.' &
  374  curl  http://172.31.0.100:8080
  375  curl  http://172.31.0.100:8080/api
  376  cd
  377  kubectl  get pods
  378  cd .kube/
  379  ls
  380  cat config
  381  cd
  382  kubectl config view
  383  kubectl config get-contexts
```
