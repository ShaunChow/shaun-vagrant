kubectl create configmap traefik-config --from-file=traefik.toml -n traefik

kubectl -n traefik create secret generic traefik-tls-cert --from-file=tls.key --from-file=tls.crt