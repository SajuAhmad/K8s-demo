# K8s-demo
Demo showing using Spring cloud Framework with Kubernetes. 


## You need 

- install minikube
- install kubectl 
- openJDK-11

## hints:
- allocate more resources to your cluster : minikube start --cpus=4  --memory='4000mb'
- Disableing swapp might improve speed
	```console
	    foo@bar:~$ minikube ssh
		$ sudo swapoff -a
	``` 



An account on: https://hub.docker.com


## optional 
check : https://kubernetes.io/docs/reference/kubectl/cheatsheet/#kubectl-autocomplete


## notes:
services are exposed as NodePort
check services : kubectl get services
get IP of the Node : kubectl cluster-info
Then call your service <NODE IP>:<NODE PORT>

to store secrets, pass them first thourgh base64: check  https://kubernetes.io/docs/concepts/configuration/secret/

# If you are having problem with minikube and Virtualbox-6 (in case error starting minikube)
apt install linux-headers-generic
dpkg-reconfigure virtualbox-dkms
dpkg-reconfigure virtualbox

(NOTE: Use firefox (if using ubuntu) to access your kubernetes deshboard or you might have some errors related to linux sendbox)
