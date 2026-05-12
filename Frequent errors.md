K8's frequent errore

1) crashloopbackoff error pods
   -> due mis-configeration of environment variables , if mis dependencies or Bad application code

Troubel shoot :
        1) describe Pod
        
2)Image pull backoff: if we give wrong image, wrong docker hub credentails  ,if we give image tag, if image is private when we won't give cred,
Troubel shoot :
        1) describe pod
        2) check the secret 
        3) check either image existed in registry or not
        
3)oom Kill : conatiner exceeds using of memory limit (over using memory )
 Troubel shoot :
           1)increase PVC , delete unamanted data from the container
4) CPU Throttling :over cpu Consumptiom 
      Troubel shoot :
          1) keep limits and requests to the container

5) Insufficeint ip -addresss
     Troubel shoot :
            1) will modify subnets on VPC
6) PV in pending state
     Troubel shoot :
             1) missmatch of stoarge classes or EBS exceed
   increase EBS volume size
   storage class sizeNO
7) NOde disk pressure
             node running out of disc causing pod eviction
   Troubel shoot :
         kubctl top nodes
   
9) Node not reday
         when the node is not in ready state
   Troubel shoot :
      kubectl describe node node-id
10) POD pending state
         no resources available (no sufficient cpu 0r RAM not avaialable in worker node)
    Troubel shoot :
       eother autosacle server or reduse the limitations of a pod
11) unauthorised acess (when we dont have permissions to access the resources )
          Troubel shoot :
12) seceret mimanagemnet
         its happe when API'S gets expire exposing the secrets on logs
    
    
    
  logs
  describe
  top (kubtl top pod)


1)  what Kubernetes networking & how it works

  to assign ip address for POD
  to provide ip & DNS name ,port for services

2) what are PV & PVC
   PV
   PVC
   used to decouple 

4) how kuberentes auto scalling works
     horizpnal pod
     vertical pod 

6) how do you debug kubernetes pods
       describe
       logs
      exec
      events
      kubctl top
   7) ROLLING UPDATES WORKS
      
   when we update images for the deployment, The deployment will create a new replica set from the replica set new pods created
   whenever new pods created from replica set the old pod will deleted from replica set
   the traffic will routed to new replica set
   8) what ingress in kubernetes how does it work
          used to ammage the external traffic ( http) host based & path based routed 
   
   9) pods resoucres need to grow beyond the limits
   
   10) what are sidecar conatiner or helpers conatiners
       useuvally pod coantins two containers
        primary conatiner where application going to run
       seconday conatiner whoc helps to primary conatiner for run application
            take backup
       storing config file passing keys
   11) QOS
       
   
   
   
  
      
      

   
  
