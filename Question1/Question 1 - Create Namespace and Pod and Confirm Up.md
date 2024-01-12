`kubectl create namespace ckad
`kubectl get namespaces | grep ckad
`kubectl config set-context --current --namespace=ckad (set current ns to ckad)
`kubectl get pods (should show no pods in namespace ckad)
`kubectl run pod1 --image=nginx --port=80 --dry-run=client -o yaml > q1.yaml
`kubectl create -f q1.yaml (check the pod exists and is running)
`kubectl describe pod pod1 | grep IP ...OR... kubectl get pods -o wide
`kubectl run busybox --image=busybox --rm -it -- bin/sh (you will now be inside the temp container)
`wget 10.128.2.8 (IP found two steps back)
`exit (exit temp container)
`kubectl logs pod1 (you should see the wget from the temp container in the logs)
`kubectl delete -f q1.yaml
`kubectl delete namespace ckad

