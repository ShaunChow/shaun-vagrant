# Command

## I. Create Namesapce 'elastic-search'

kubectl create namespace elastic-search

## II. Install elastic-cloud-operator 

Follow install guide 7_operator/elastic-cloud-operator 

## III. Install elastic-search

kubectl apply -f elastic-search-deploy.yaml -n elastic-search


## IV. Create Namesapce 'kibana'

kubectl create namespace kibana

## V. Install kibana

kubectl apply -f kibana-deploy.yaml -n kibana

kubectl apply -f kibana-ingress.yaml -n kibana