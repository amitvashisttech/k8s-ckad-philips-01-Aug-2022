```
  178  cd 05-Service/
  179  ls
  180  cat 01-helloworld.yaml
  181  kubectl  apply -f 01-helloworld.yaml
  182  kubectl  get pods
  183  kubectl  get pods -o wide
  184  kubectl  get svc
  185  kubectl expose rc helloworld-controller
  186  kubectl  get svc
  187  kubectl  edit svc helloworld-controller
  188  kubectl  get svc
  189  kubectl  edit svc helloworld-controller
  190  kubectl  get svc
  191  kubectl  get pods -n kube-system
  192  kubectl  get pods -o wide
  193  kubectl  get nodes -o wide
  194  kubectl  delete pod --all
  195  kubectl  get pods -o wide
  196  kubectl  describe svc helloworld-controller
  197  kubectl  get pods --show-labels
  198  kubectl scale --replicas=1 rc helloworld-controller
  199  kubectl  get pods --show-labels
  200  kubectl  get pods -o wide
  201  kubectl  describe svc helloworld-controller
  202  kubectl scale --replicas=3 rc helloworld-controller
  203  kubectl  get pods -o wide
  204  kubectl  get pods --show-labels
  205  kubectl  get pods -o wide
  206  kubectl  describe svc helloworld-controller
  207  ls
  208  kubectl  apply -f 03-app-svc-deployment.yaml
  209  kubectl  get pods
  210  kubectl  get svc
  211  kubectl  get pods -o wide
  212  cd ..
  213  ls
  214  cd 04-Replication-Cantroller/
  215  ls
  216  vim helloworld-rc.yaml
  217  ls
  218  cd ..
  219  ls
  220  cd 05-Service/
  221  ls
  222  cat 01-helloworld.yaml
  223  kubectl  get svc
  224  kubectl  delete svc  helloworld-controller
  225  kubectl  get svc
  226  ls
  227  vim 02-helloworld-svc.yaml
  228  kubectl  apply -f 02-helloworld-svc.yaml
  229  kubectl  get svc
  230  cat 01-helloworld.yaml
  231  cat 02-helloworld-svc.yaml
  232  kubectl  describe svc helloworld-service
  233  ls
  234  kubectl  get svc
  235  kubectl api-resources
  236  ls
  237  kubectl  get svc
  238  kubectl  edit  svc helloworld-service
  239  kubectl  get svc
  240  ls
  241  cd ..
  242  ls
  243  git add . ; git commit -m "05-Service" ; git push
```
