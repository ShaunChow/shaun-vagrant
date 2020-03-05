# Command

## I. Create Namesapce 'vitess'

kubectl create namespace vitess

## II. Install etcd-operator 

Follow install guide 7_operator/etcd_operator

## III. Create Database password

kubectl create secret generic myuser-password --from-literal=password=abc123 -n vitess

## IV. Deploy Vitess

kubectl apply -f vitess-deploy.yaml -n vitess

## V. Install ingress

kubectl apply -n vitess -f vitess-ingress.yaml

# Uninstall

kubectl delete -f vitess-deploy.yaml -n vitess