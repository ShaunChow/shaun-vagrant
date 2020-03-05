
# Command

## I. Create Namesapce 'mysql'

kubectl create namespace mysql

## II. Install mysql via helm3

helm install mysql stable/mysql -n mysql -f helm-config.yaml

***
kubectl port-forward -n mysql svc/mysql 3306

login to DB create database keycloak for serverless application Keycloak