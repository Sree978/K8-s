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
   storage class size
7) NOde disk pressure
     Troubel shoot :
           node running out of disc causing pod eviction 
9) 
      
      

   
  
