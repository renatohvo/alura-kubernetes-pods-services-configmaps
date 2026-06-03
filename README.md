# [Kubernetes: Pods, Services e ConfigMaps - Alura](https://www.alura.com.br/curso-online-kubernetes-pods-services-configmap?srsltid=AfmBOoqY8Y5sqOoCngOvBYqQfYLvT8Q7Q0SDEBm0WaiQCbQnXFmxCE-W)

## Install

kubectl:

```sh
sudo apt-get install curl -y
curl -LO "https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl"
chmod +x ./kubectl
sudo mv ./kubectl /usr/local/bin/kubectl
```

minikube:

```sh
curl -Lo minikube https://storage.googleapis.com/minikube/releases/v1.12.1/minikube-linux-amd64 \ && chmod +x minikube
sudo install minikube /usr/local/bin/
```

## Pods - Modo Imperativo

- Create Pod (nginx)

```sh
kubectl run nginx-pod --image=nginx:latest
```

- Describe Pod (nginx)

```sh
kubectl describe pod nginx-pod
```

- Edit Pod (nginx)

```sh
kubectl edit pod nginx-pod
```

- Delete Pod (nginx)

```sh
kubectl delete pod nginx-pod
```

## Pods - Modo Declarativo

- Apply Pod

```sh
kubectl apply -f ./primeiro-pod.yaml
```

- Delete Pod

```sh
kubectl delete -f ./primeiro-pod.yaml
```
