
# Command

## I. Create Namesapce 'proxysql'

kubectl create namespace proxysql

## II. Create Config

kubectl apply -f proxysql-config.yaml -n proxysql

## III. Create Service & Deployment

kubectl apply -f proxysql-deploy.yaml -n proxysql