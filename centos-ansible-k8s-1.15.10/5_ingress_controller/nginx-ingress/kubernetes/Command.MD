

# Command

## I. Create Namesapce 'kubernetes-nginx-ingress'

kubectl create namespace kubernetes-nginx-ingress

## II. Install kubernetes/nginx-ingress via helm3

helm install kubernetes-nginx-ingress stable/nginx-ingress -n kubernetes-nginx-ingress -f helm-config.yaml