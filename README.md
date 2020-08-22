# reeps-k8s
raspberry pi3b kubernetes cluster

# installation

1. first install traefik-rbac.yaml
2. then install traefik-daemonset.yaml
3. then install metallib.yaml
4. then metallb-configmap.yaml
5. install wordpress-mysql which uses linuxserver/mariadb rather than mysql
6. then install wordpress-deployment

NOTE: strip the passwords; else you won't be able to connect to db
tr -d '\n' <password.txt >.strippedpassword.txt && mv .strippedpassword.txt password.txt

kubectl create secret generic mariadb-pass --from-file=mariadb-secret.txt
https://hub.docker.com/r/linuxserver/mariadb

To Install Flannel (in lieue of weave-net)
```
curl -sSL https://raw.githubusercontent.com/coreos/flannel/v0.12.0/Documentation/kube-flannel.yml | kubectl apply -f -
```
