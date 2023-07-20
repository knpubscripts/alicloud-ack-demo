# alicloud-ack-demo
### Provision Alibaba Cloud Infrastructure using Terraform

clone source code from this repo to provision the infrastructure on Alibaba Cloud using terraform configuration:

```git clone https://github.com/knpubscripts/alicloud-terraform.git```

Wait about 10-15 minutes to ACK cluster created, go to: Cluster Information > Connection Information > Public Access (tab) > Copy the content to $HOME/.kube/config on your local computer.

Then you can use the kubectl to interact and control ACK cluster from your computer.

### kubectl apply commands in order
```
    kubectl apply -f mongo-secret.yaml
    kubectl apply -f mongo.yaml
    kubectl apply -f mongo-configmap.yaml
    kubectl apply -f mongo-express.yaml
    kubectl apply -f nginx-ingress.yaml
```
### kubectl get commands
```
    kubectl get pod
    kubectl get pod --watch
    kubectl get pod -o wide
    kubectl get service
    kubectl get secret
    kubectl get all | grep mongodb
```
### kubectl debugging commands
```
    kubectl describe pod mongodb-deployment-xxxxxx
    kubectl describe service mongodb-service
    kubectl logs mongo-express-xxxxxx
```
