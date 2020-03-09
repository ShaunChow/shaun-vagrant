

# Command

## I. Create Namesapce 'weave-scope'

kubectl create namespace weave-scope

## II. Install weave-scope via helm3

helm install weave-scope stable/weave-scope -n weave-scope -f helm-config.yaml
