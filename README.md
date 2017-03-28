# Deploy the secret
kubectl create secret generic cookwell-redirect-pod-config --from-file=config.js

# Deploy the NodePort service
kubectl apply -f nginx.service.yml

# Deploy the pod
kubectl apply -f nginx.pod.yml

# Deploy the ingress controller
kubectl apply -f ingress.yml
