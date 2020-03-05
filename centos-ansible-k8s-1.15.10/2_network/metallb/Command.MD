

# Command

## I. Create Namesapce 'metallb'

kubectl create namespace metallb

## II. Install metallb via helm3

helm install metallb stable/metallb -n metallb -f helm-config.yaml