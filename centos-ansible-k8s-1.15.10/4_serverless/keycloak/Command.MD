
# Command

## I. Create Namesapce 'keycloak'

kubectl create namespace keycloak

## II. Add certs into k8s secret

--Generate:

openssl req -x509 -nodes -days 365 -keyout tls.key -out tls.crt -subj "/CN=shaun.io"

kubectl create secret tls keycloak-tls --key="certs/tls.key" --cert="certs/tls.crt" -n keycloak

## III. Install keycloak via helm3

helm install keycloak codecentric/keycloak -n keycloak -f helm-config.yaml

## IV. Install ingress

kubectl apply -n keycloak -f keycloak-ingress.yaml

## Uninstall

kubectl delete -n keycloak -f keycloak-ingress.yaml