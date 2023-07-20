# alicloud-ack-demo
### Install kubectl (Kubernetes Client tool):
The Kubernetes command-line tool, kubectl, allows you to run commands against Kubernetes clusters. You can use kubectl to deploy applications, inspect and manage cluster resources, and view logs. For more information including a complete list of kubectl operations, see the [```kubectl```][kubectl_doc_link] reference documentation.

kubectl is installable on a variety of Linux platforms, macOS and Windows. Find your preferred operating system below.

[Install kubectl on Linux][kubectl_linux_link]

[Install kubectl on macOS][kubectl_mac_link]

[Install kubectl on Windows][kubectl_win_link]

[kubectl_linux_link]: https://kubernetes.io/docs/tasks/tools/install-kubectl-linux
[kubectl_mac_link]: https://kubernetes.io/docs/tasks/tools/install-kubectl-macos
[kubectl_win_link]: https://kubernetes.io/docs/tasks/tools/install-kubectl-windows
[kubectl_doc_link]: https://kubernetes.io/docs/reference/kubectl/

### Provision Alibaba Cloud Infrastructure using Terraform

clone source code from this repo to provision the infrastructure on Alibaba Cloud using terraform configuration:

```git clone https://github.com/knpubscripts/alicloud-terraform.git```

Or visit the repo link to see the details: https://github.com/knpubscripts/alicloud-terraform

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
