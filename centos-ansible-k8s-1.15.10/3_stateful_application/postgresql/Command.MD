
# Command

## I. Create Namesapce 'postgresql'

kubectl create namespace postgresql

## II. Install postgresql via helm3

helm install postgresql stable/postgresql -n postgresql -f helm-config.yaml

***
kubectl port-forward --namespace postgresql svc/postgresql 5432:5432

login to DB create database keycloak for serverless application Keycloak