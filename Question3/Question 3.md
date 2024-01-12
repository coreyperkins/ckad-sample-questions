`kubectl create secret generic db-credentials --from-literal=db_password=speed`
`kubectl get secrets`
`kubectl run backend --image=nginx --dry-run=client -o yaml > q3.yaml`
`kubectl create -f q3.yaml`
`kubectl get pods`
`kubectl exec backend -it -- /bin/sh`