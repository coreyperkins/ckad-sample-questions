`kubectl run secured --image=nginx --dry-run=client -o yaml > q4.yaml`
`kubectl create -f q4.yaml`
`kubectl exec secured -it -- /bin/sh`
(inside the container now cd /data/app and create a new file via touch and check the group is 3000 with ls -al)