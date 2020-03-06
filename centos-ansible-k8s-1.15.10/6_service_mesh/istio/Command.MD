# Install istio-system

istioctl manifest apply \
 --set profile=demo \
 --set hub=dockerhub.azk8s.cn/istio \
 --set values.kiali.hub=quay.azk8s.cn/kiali \
 --set values.prometheus.hub=dockerhub.azk8s.cn/prom \
 --set values.tracing.jaeger.hub=dockerhub.azk8s.cn/jaegertracing \
 --set values.tracing.opencensus.hub=dockerhub.azk8s.cn/omnition \
 --set values.tracing.zipkin.hub=dockerhub.azk8s.cn/openzipkin

# Install ingress

kubectl apply -f istio-ingress.yaml -n istio-system

# Uninstall

kubectl delete -f istio-ingress.yaml -n istio-system

kubectl delete -f istio-manifest-v1.5.0.yaml -n istio-system