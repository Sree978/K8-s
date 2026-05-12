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
      
      

   
  
