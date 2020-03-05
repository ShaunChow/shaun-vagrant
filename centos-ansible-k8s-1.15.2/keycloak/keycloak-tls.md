
openssl req -x509 -nodes -days 365 -keyout tls.key -out tls.crt -subj "/CN=shaun.io"

kubectl create secret tls keycloak-tls --key="tls.key" --cert="tls.crt" --namespace keycloak