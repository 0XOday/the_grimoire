![[Pasted image 20250606183429.png]]


the components of k8s
* Control plan
	* make global decisions about the cluster like scheduling starting new pods 
	* can be ran on any machine in the cluster
	* does not run containers on the control plan ( I do not know why my box has containers running )
	* we can crate a highly available cluster with kubeadm 
* Kube-apiserver
	* Componet of the control plane 
	* the API server is the front end for the control plane 
	* we can run more than one api-server to load balance 
* 