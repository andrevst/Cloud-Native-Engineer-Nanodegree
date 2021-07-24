# Exercises

## lesson 3.21

```shell
# create namespace
kubectl create ns demo
# label namespace
kubectl label ns demo tier=test
# create nginx deploy  
kubectl create deploy nginx-alpine --image=nginx:alpine -n demo
# can use --replicas=3
# scale replicas from 1 to 3
kubectl scale --current-replicas=1 --replicas=3 deployment/nginx-alpine --namespace demo
# label deployment
kubectl label deploy nginx-alpine app=nginx tag=alpine --namespace demo
# expose deployment, which will create a service
kubectl expose deployment nginx-alpine --port=8111 --namespace demo
# create a config map
kubectl create configmap nginx-version --from-literal=version=alpine --namespace demo
```

- reference:
  - [kubectl cheatsheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)