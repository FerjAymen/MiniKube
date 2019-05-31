# MiniKube
script to install and test Kubernetes locally
Minikube is a tool that quickly spin up a local single machine with a k8s cluster.
it aimed on users who want to just test it out or use it foe development. 
Minikube is a one node machine with no high availabilty. 

to run this script properly you need:
1/ linux distribution
2/ oracle virtualbox : hypervisor installed and enabled 
3/ giving execution permission to the file : chmod +x minikube

to run the script : ./minikube 
this will download the minikube tool and install it then add it to the executable path
instal the kubectl command and add it to the executable path . 
start a minikube cluster 

after executing the script you will have a kubernets cluster started locally on your machine .


* you can create a Kubernetes deployment with this command : kubectl run hello-minikube 
example : Let’s create a Kubernetes Deployment using an existing image named echoserver, which is a simple HTTP server and expose it on port 8080 using --port : kubectl run hello-minikube --image=k8s.gcr.io/echoserver:1.10 --port=8080

*To access the hello-minikue Deployment, expose it as a Service: kubectl expose deployment hello-minikube --type=NodePort

*check the status of the pod : kubectl get pod

*Get the URL of the exposed Service to view the Service details: minikube service hello-minikube --url
copy and paste the url on your borwser to view the details of you the cluster . 

* to stop the local cluster run : minikube stop

*if you want to delete the service : kubectl delete services name_of_the_service ( in this case hello-minikube)

*if you want to delete the deployment: kubectl delete deployment name_of_deployment 
