
# Command

## I. Create Namesapce 'kong'

kubectl create namespace kong

## II. Add tls secret

openssl req -x509 -nodes -days 365 -keyout tls.key -out tls.crt -subj "/CN=shaun.io"

kubectl -n kong create secret generic kong-proxy-tls --from-file=certs/tls.key --from-file=certs/tls.crt

## III. Install kong via helm3

helm install kong kong/kong -n kong -f helm-config.yaml


# Uninstall

kubectl delete crd kongconsumers.configuration.konghq.com

kubectl delete crd kongcredentials.configuration.konghq.com

kubectl delete crd kongingresses.configuration.konghq.com

kubectl delete crd kongplugins.configuration.konghq.com

# Tips

Kong Https Setting:

    - Add Kong annotations to your https service
    eg: 
        annotations:
                configuration.konghq.com/protocol: https
