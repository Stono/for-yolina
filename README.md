# Certs
You need to add your TLS certs (wildcard, and EV) to cookwell-www and cookwell (or rename them in the ingress file).

# Deploy the config secret
kubectl create secret generic cookwell-redirect-pod-config --from-file=config.js

# Deploy the NodePort service
kubectl apply -f nginx.service.yml

# Deploy the Pod
kubectl apply -f nginx.pod.yml

# Deploy the Ingress
kubectl apply -f ingress.yml
