# tsung
First, create `tsung` namespace.

```
kubectl create ns tsung
```
Now, create target deployment.

```
kubectl apply -f target.yaml
```

Then, for tsung cluster needs to create slave first. then needs to create master. 

```
kubectl apply -f tsung-slave.yaml # create slave, wait for pods to go into running state.
kubectl apply -f tsung-master.yaml 
```

you can see target pods logs by

```
kubectl logs -f <pod-name> -n tsung
```
