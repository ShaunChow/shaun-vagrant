

# Command

## I. Create Namesapce 'redis-ha'

kubectl create namespace redis-ha

## II. Install redis-ha via helm3

helm install redis-ha stable/redis-ha -n redis-ha -f helm-config.yaml


# Uninstall

helm uninstall redis-ha -n redis-ha


