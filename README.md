# eks_terraform

EKS Terraform - build an EKS cluster using Hashicorp's popular tutorial, then 
create first deployment using Nigel Poulton's The Kubernetes Book tutorial...    



<pre>

Clone the repo.

Build the cluster in the Terraform directory:

# cd terraform
# terraform init
# terraform validate
# terraform plan
# terraform apply -auto-approve  

Cluster takes about 10 minutes to provision.  


# cd ../deployment
# kubectl apply -f deploy.yml
# kubectl apply -f lb.yml

...

scottghome@scottgs-MBP deployments % kubectl get pods
NAME                           READY   STATUS    RESTARTS   AGE
hello-deploy-97668bd59-2wtjv   1/1     Running   0          9s
hello-deploy-97668bd59-7jz6m   1/1     Running   0          9s
hello-deploy-97668bd59-95hhs   1/1     Running   0          9s
hello-deploy-97668bd59-9npvn   1/1     Running   0          9s
hello-deploy-97668bd59-f9p9f   1/1     Running   0          9s
hello-deploy-97668bd59-j7w8b   1/1     Running   0          9s
hello-deploy-97668bd59-t9d5f   1/1     Running   0          9s
hello-deploy-97668bd59-vbhmk   1/1     Running   0          9s
hello-deploy-97668bd59-vr55m   1/1     Running   0          9s
hello-deploy-97668bd59-zdw7w   1/1     Running   0          9s

...

scottghome@scottgs-MBP deployments % kubectl get svc lb-svc
NAME     TYPE           CLUSTER-IP       EXTERNAL-IP                                                              PORT(S)          AGE
lb-svc   LoadBalancer   172.20.217.201   a9ea19b2f379b41a9a7efdf269cbffa4-961409687.us-east-2.elb.amazonaws.com   8080:32463/TCP   12s

Visit the EXTERNAL-IP url, port 8080. 

</pre>
