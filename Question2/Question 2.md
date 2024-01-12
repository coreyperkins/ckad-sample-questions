`kubectl create namespace ckad`
`kubectl config set-context --current --namespace=ckad`
`kubectl create configmap db-config --from-env-file=config.env`
`kubectl get configmap`
`kubectl run sqlsrv --image=nginx --dry-run=client -o yaml > q2.yaml`
`kubectl create -f q2.yaml`
`kubectl get pods`
`kubectl exec sqlsrv -it -- bin/sh`
`printenv` (you are inside the shell this should show env vars from the configmap)