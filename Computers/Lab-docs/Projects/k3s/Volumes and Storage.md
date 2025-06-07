* K3s comes with Rancher's Local Path Provisioner and this enables the ability to create persistent volume claims out of the box using local storage on the respective node.
* k3s also supports longhorn
	* setting up storage via a yaml file called pvc 
```
apiVersion: v1
kind: PersistentVolumeClaim
metadata:  
name: local-path-pvc  
namespace: default
spec:  
	accessModes:    
	- ReadWriteOnce  
	storageClassName: local-path  resources:    
	requests:      
	storage: 2Gi
```

* `kubectl delete pvc --all `
