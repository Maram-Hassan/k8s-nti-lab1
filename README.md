# k8s-nti-lab1
# k8s-nti-lab1
1- Install ka cluster Iminskabel toptiooni you can use http://www.katacoda.com/courses/kubernetes/playgrounds

2-Create a pod with the name redis and with the image redis. 

3- Creats a pod with the name nginx and with the image "nginx123" Use a pod definition YAML

4-What is the nginx pod status?
```
ImagePullBackOff
```
5-change the nginx pod image to "nginx" check the status again?
```
runing
```
6-how many replicaset exist on system?
```
0
```
7- create a replicaset with name =replica-set-1,image=busybox,replicas=3

8-Scale the replicaset replica-set-1 to 5 pods 

9- How many PODs are READY in the replica-set-1?
```
3
```
10- Delete any one of the POD then check How many PODs exist now? Why are there still 5 PODs, even efter you deleted one
```
5 , beacuse replicaset scale it to 5 even if one is deleted or failed
```
11- How many Deployments and Replicasets exist on the system? 
```
0,1
```
12- create a Deployment with name deployment-1 Imaga busybox replicas 3

how many Deployments and Replicalleats exist on the system now? 
```
1,1
```
14- How many pods are ready with the deployment-1
```
3
```
15-Update deployment-1 image to nginx then check the ready pod again
16- Run kubectl describe deployment deployment-1 and check events
 What is the deployment strategy used to upgrade the deployment-1
 ```
RollingUpdate
```
19 - Rollback the deployment-1
What is the used image with the deployment-1?
```
busybox
```
18- Create a deployment using nginx image with latest tag only and remember to mention tag i.e nginx:latest and name it as nginx-deployment. App labels should be app:nginx-app and type:front-end. The container should be named an nginx-containers also make sure replicas counts are 3.
