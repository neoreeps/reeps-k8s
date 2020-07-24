# reeps-k8s
raspberry pi3b kubernetes cluster

# installation

## first install traefik-rbac.yaml

## then install traefik-daemonset.yaml
Which is actually service, daemonset, ui 

## then install metallib.yaml
## then metallb-configmap.yaml

# install wordpress-mysql which uses linuxserver/mariadb rather than mysql
# strip th damn passwords
tr -d '\n' <password.txt >.strippedpassword.txt && mv .strippedpassword.txt password.txt

kubectl create secret generic mariadb-pass --from-file=mariadb-secret.txt
https://hub.docker.com/r/linuxserver/mariadb

