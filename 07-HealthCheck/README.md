```
687  cd 07-HealthCheck/
  688  ls
  689  vim 01-helloworld-deploy-hc.yaml
  690  kubectl  get pods
  691  kubectl  apply -f 01-helloworld-deploy-hc.yaml
  692  kubectl  get pods
  693  kubectl  describe pod python-webapp-deployment-5679955cb7-2hrb5
  694  kubectl  get pods
  695  kubectl  describe pod helloworld-deployment-66fd77b9f-bnp8z
  696  kubectl  get pods
  697  kubectl  delete -f ../06-Service/app-svc-deployment.yaml
  698  ls
  699  kubectl  get pods
  700  kubectl edit deploy helloworld-deployment
  701  kubectl  get pods
  702  kubectl  describe pod helloworld-deployment-6d68bd8cff-4jxrs
  703  watch -n .5 kubectl get pods -o wide
  704  ls
  705  vim 02-helloworld-deploy-custom-values.yaml
  706  kubectl  apply -f 02-helloworld-deploy-custom-values.yaml
  707  kubectl  get pods
  708  kubectl  apply -f 01-helloworld-deploy-hc.yaml
  709  kubectl  get pods
  710  kubectl  describe pod helloworld-2-deployment-69ddc54654-jbpqm
  711  ls
  712  kubectl  delete -f 01-helloworld-deploy-hc.yaml 02-helloworld-deploy-custom-values.yaml
  713  kubectl  delete -f 01-helloworld-deploy-hc.yaml
  714  kubectl  delete -f 02-helloworld-deploy-custom-values.yaml
  715  ls
  716  vim 03-pod-prob-exec.yaml
  717  ls
  718  kubectl apply -f 03-pod-prob-exec.yaml
  719  kubectl  get pods
  720  kubectl describe pod liveness-exec
  721  kubectl  get pods
  722  watch -n .5 kubectl get pods -o wide
  723  ls
  724  kubectl  get pods
  725  kubectl  exec -it liveness-exec -- ls -ltr /tmp
  726  kubectl  exec -it liveness-exec -- cat /tmp/healthy
  727  kubectl  get pods
  728  kubectl  exec -it liveness-exec -- cat /tmp/healthy
  729  kubectl  exec -it liveness-exec -- ls -ltr /tmp
  730  kubectl  get pods
  731  kubectl  describe pod liveness-exec
  732  kubectl  get pods
  733  kubectl  exec -it liveness-exec -- ls -ltr /tmp
  734  kubectl  exec -it liveness-exec -- cat /tmp/healthy
  735  ls
  736  kubectl  delete -f 03-pod-prob-exec.yaml
  737  ls
  738  vim 04-helloworld-deploy-readiness-healthcheck.yaml
  739  ls
  740  kubectl  apply 04-helloworld-deploy-readiness-healthcheck.yaml
  741  kubectl  apply -f 04-helloworld-deploy-readiness-healthcheck.yaml
  742  kubectl  get pods
  743  kubectl  describe pod helloworld-deployment-77b548f7d-rbdj5
  744  kubectl  edit deploy
  745  watch -n .5 kubectl get pods -o wide
  746  ls
  747  kubectl  delete -f 04-helloworld-deploy-readiness-healthcheck.yaml
```
