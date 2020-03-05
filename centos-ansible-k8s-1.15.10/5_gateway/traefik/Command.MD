
# Command

## I. Create Namesapce 'traefik'

kubectl create namespace traefik

## II. Create Custom Resource Definition

kubectl apply -f traefik-crd.yaml -n traefik

## III. Create ServiceAccount & RoleBinding

kubectl apply -f traefik-rbac.yaml -n traefik


## IV. Add tls secret

openssl req -x509 -nodes -days 365 -keyout tls.key -out tls.crt -subj "/CN=shaun.io"

kubectl -n traefik create secret generic traefik-tls-cert --from-file=certs/tls.key --from-file=certs/tls.crt

## V. Add Config

kubectl apply -f traefik-config.yaml -n traefik

## VI. Create Deployment

kubectl apply -f traefik-deploy.yaml -n traefik

## VII. Create Service

kubectl apply -f traefik-service.yaml -n traefik

## VIII. Create IngressRoute

kubectl apply -f traefik-ingress.yaml -n traefik