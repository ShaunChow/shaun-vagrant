# Command

## I. Create Namesapce 'kubernetes-dashboard'

kubectl create namespace kubernetes-dashboard

## II. Install kubernetes-dashboard via helm3

kubectl create secret tls kubernetes-dashboard-tls --key="certs/tls.key" --cert="certs/tls.crt" -n kubernetes-dashboard

helm install kubernetes-dashboard stable/kubernetes-dashboard -n kubernetes-dashboard -f helm-config.yaml

## III. Install ingress

kubectl apply -n kubernetes-dashboard -f k8s-dashboard-ingress.yaml

## Uninstall

kubectl delete -n kubernetes-dashboard -f k8s-dashboard-ingress.yaml

helm uninstall kubernetes-dashboard -n kubernetes-dashboard 

# kubernetes-dashboard v2

https://github.com/kubernetes/dashboard

https://raw.githubusercontent.com/kubernetes/dashboard/v2.0.0-rc5/aio/deploy/recommended.yaml

kubectl apply -f k8s-dashboard-v2-deploy.yaml -n kubernetes-dashboard

kubectl create secret tls kubernetes-dashboard-tls --key="certs/tls.key" --cert="certs/tls.crt" -n kubernetes-dashboard

kubectl apply -n kubernetes-dashboard -f k8s-dashboard-ingress.yaml