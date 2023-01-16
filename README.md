1. Deployment
```
$ kubectl create deployment hello-node --image=k8s.gcr.io/echoserver:1.4
$ kubectl get deployments
$ kubectl get pods
$ kubectl get events
$ kubectl config view
```

2. Service
```
$ kubectl expose deployment hello-node --type=LoadBalancer --port=8080
$ kubectl get services
$ minikube service hello-node
```

3. Add-on
```
$ minikube addons list
$ minikube addons enable metrics-server
$ kubectl get pod,svc -n kube-system
$ minikube addons disable metrics-server
```

4. Clean up
```
$ kubectl delete service hello-node
$ kubectl delete deployment hello-node
```
