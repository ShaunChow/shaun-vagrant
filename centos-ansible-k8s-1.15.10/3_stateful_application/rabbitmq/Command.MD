

# Command

## I. Create Namesapce 'rabbitmq-ha'

kubectl create namespace rabbitmq-ha

## II. Install rabbitmq-ha via helm3

helm install rabbitmq-ha stable/rabbitmq-ha -n rabbitmq-ha -f helm-config.yaml

## III. Install ingress for rabbitmq management

kubectl apply -f rabbitmq-management-ingress.yaml -n rabbitmq-ha


# Update

$ export ERLANGCOOKIE=$(kubectl get secrets -n rabbitmq-ha rabbitmq-ha-rabbitmq-ha -o jsonpath="{.data.rabbitmq-erlang-cookie}" | base64 --decode)
$ helm upgrade rabbitmq-ha stable/rabbitmq-ha  -f helm-config.yaml

# Uninstall

helm uninstall rabbitmq-ha -n rabbitmq-ha