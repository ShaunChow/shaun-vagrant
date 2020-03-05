
# Command

## I. Create Namesapce 'nfs-client-provisioner'

kubectl create namespace nfs-client-provisioner

## II. Install nfs-client-provisioner via helm3

helm install nfs-client-provisioner stable/nfs-client-provisioner -n nfs-client-provisioner -f helm-config.yaml