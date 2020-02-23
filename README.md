![Docker Pulls](https://img.shields.io/docker/pulls/keaz/jenkins-slave?label=Jenkins%20Slave%20docker%20pulls)
![Docker Pulls](https://img.shields.io/docker/pulls/keaz/jenkins-master?label=Jenkins%20Master%20docker%20pulls)
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
https://www.youtube.com/watch?v=768SxaFkvQ4

###### docker jenkins-master 
https://hub.docker.com/repository/docker/keaz/jenkins-master

###### docker jenkins-slave 
https://hub.docker.com/repository/docker/keaz/jenkins-slave

### 2020/02/08
New Jenkins master image keaz/jenkins-master:alpine

New Jenkins slave image keaz/jenkins-slave:slim
