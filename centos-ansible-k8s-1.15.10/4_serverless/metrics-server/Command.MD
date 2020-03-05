

# Command

## I. Create Namesapce 'metrics-server'

kubectl create namespace metrics-server

## II. Install metrics-server via helm3

helm install metrics-server stable/metrics-server -n metrics-server -f helm-config.yaml
