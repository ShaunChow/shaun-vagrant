
# Prerequisite

NFS Server:
    server: 172.17.8.1
    path: /Users/srv/nfs/kubedata/

CA:
    For yourself dns ,eg: shaun.io  -- this is mine.

    172.17.8.104 dashboard.shaun.io

    172.17.8.104 traefik.shaun.io

    172.17.8.104 keycloak.shaun.io

    172.17.8.104 rabbitmq.shaun.io

    172.17.8.104 vtgate.vitess.shaun.io
    172.17.8.104 vtctld.vitess.shaun.io

    172.17.8.104 kibana.shaun.io

    172.17.8.104 prometheus.istio.shaun.io
    172.17.8.104 kiali.istio.shaun.io
    172.17.8.104 grafana.istio.shaun.io
    172.17.8.104 jaeger.istio.shaun.io

    172.17.8.104 weave-scope.shaun.io

    172.17.8.105 tcp.shaun.io
    172.17.8.105 udp.shaun.io

    tcp:
        redis   tcp.shaun.io:6379

Helm 3

Istioctl

Kubectl

Machine Ip:
    kmaster 172.17.8.101
    kworker1 172.17.8.102
    kworker2 172.17.8.103

Pod Network cidr:
    192.168.0.0/16

VirtualBox

Vagrant

Ansiable

# Load Balance for Ingress

    traefik 172.17.8.104
    kubernetes/nginx-ingress 172.17.8.105
    kong 172.17.8.106


# Docker Repository Mirror Recommand:

http://mirror.azure.cn/


dockerhub.io --> dockerhub.azk8s.cn
quary.io --> quay.azk8s.cn
gcr.io --> gcr.azk8s.cn

# Kubernetes Proxy Rule:

kubectl proxy --port=8080 

http://localhost:8080/api/v1/proxy/namespaces/<NAMESPACE>/services/<SERVICE-NAME>:<PORT-NAME>/ 

# Kubernetes Service Local DNS Rule:


# etc...