# Jenkins for K8s

This is an reference project that aims to explains how to run a Jenkins cluster in K8s.

###### PVC
PVC in this project is created for Kubernetes provided by **Docker for Mac**. This can be use in minikube as well. Please change the hostPath in the **jenkins-pv.yaml**.
```
apiVersion: v1
kind: PersistentVolume
metadata:
  name: jenkins-volume
  labels:
    type: local
spec:
  storageClassName: manual
  capacity:
    storage: 10Gi
  accessModes:
    - ReadWriteOnce
  hostPath:
    path: "<your host path>"
```

https://medium.com/faun/how-to-setup-scalable-jenkins-on-kubernetes-f5c1b7d439cd
