# haco-helm

minikube start --cpus 4 --memory 8192
minikube dashboard

helm dep update
helm dep build

helm list

helm install haco . -f .\values.yaml
helm upgrade haco . -f .\values.yaml

helm uninstall haco

kubectl get pods
kubectl describe node

kubectl get pods -w
kubectl port-forward svc/haco-es-address-search-master 9200
kubectl port-forward deployment/haco-kibana 5601 