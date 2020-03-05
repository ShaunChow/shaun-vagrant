

# Command

## I. Create Namesapce 'etcd-operator'

kubectl create namespace etcd-operator

## II. Install etcd-operator

kubectl apply -n etcd-operator -f etcd_operator_rbac.yaml 

kubectl apply -n etcd-operator -f etcd_operator_deploy.yaml

## uninstall

kubectl delete -n etcd-operator -f etcd_operator_deploy.yaml

kubectl delete -n etcd-operator -f etcd_operator_rbac.yaml

kubectl delete endpoints etcd-operator

kubectl delete crd etcdclusters.etcd.database.coreos.com

kubectl delete clusterrole etcd-operator

kubectl delete clusterrolebinding etcd-operator