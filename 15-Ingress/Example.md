```
5 Service  
5 Master Node 
200 Node Clutser 
Deploy 1: 50 Pods 
Deploy 2: 100 Pods 
Deploy 3: 200 Pods 
Deploy 4: 200 Pods 
Deploy 5: 200 Pods 


Deploy 6 - 150 


=====================================>
Deploy 1 -> SVC 1 (SelfCare ) -> NodePort : 32777 ( 50IPAddress ):32777
Deploy 1 -> SVC 1 (PaymentAuth) -> NodePort : 32778 ( 100IPAddress ):32778
Deploy 1 -> SVC 1 (PaymentCapture) -> NodePort : 32779 ( 200IPAddress ):32779
Deploy 1 -> SVC 1 (Subcribtion) -> NodePort : 32780 ( 200IPAddress ):32780
Deploy 1 -> SVC 1 (Notificaton ) -> NodePort : 32781 ( 200IPAddress ):32781


=====================================>

NameSpace : Ingress 
ClusterRole: SA - Default 
Toleration : master 

Ingress Replicas : 5 

master-0..5: 

Expose RC Ingress : NodePort 

master-(0..5), SVC-Ingress (80:30808,443:30809) --> Default Backend ( Echoheader-Service ) ( Welcome to Ericsson Network, Seems like you are missing the context path in the URL for your service lookup )


Ingress Rules 

http:
      paths:
      - path: /
        backend:
          serviceName: helloworld-v1
          servicePort: 80

/SelfCare -> backend -> SVC 1 -> 32777 
/PaymentAuth -> backend -> SVC 2 -> 32778
/PaymentCapture -> backend -> SVC 3 -> 32779



curl -v  172.31.0.102:30808 ( Welcome ) 
curl -v  172.31.0.102:30808/SelfCare ( SelfCare API  ) 





Physcal LoadBalancer -> ( 10.19.11.10 ) [80,443]--> [( master-0..5):30808.30809] 


curl -v  10.19.11.10 ( Welcome ) 
curl -v  10.19.11.10/SelfCare ( SelfCare API  ) 


DNS : 

www.vodafone-ppe.com -> 10.19.11.10

curl -v   www.vodafone-ppe.com ( Welcome ) 
curl -v   www.vodafone-ppe.com/SelfCare ( SelfCare API  )
