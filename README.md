# dce-K8s-cluster

Repozitory obsahuje Kubernetes soubory deployment.yml, ingress.yml a service.yml.
Popisují cílový stav clusteru tak jak má být vytvořen prostřednictvím cubectl a nástroje minicube.

# Prerekvizity
Nainstalovaný nástroj minikube a kubectl, správnost instalace lze ověřit následujícími příkazy:

minikube status

minikube addons list | grep ingress

kubectl get nodes

kubectl get pods -A

kubectl get pods -n ingress-nginx

# Příkaz apply
Aplikace souborů se provede následujícím příkazem:

kubectl apply -f .

nebo 

kubectl apply -f deployment.yml

kubectl apply -f service.yml

kubectl apply -f ingress.yml

# Ověření

kubectl get pods

kubectl get svc

kubectl get ingress
