## Ejercicio 9

Instrucciones para desplegar y verificar el funcionamiento:

- Instalar minikube

- `minikube start`

- `alias kubectl="minikube kubectl --"`

- Escribir el archivo deplyment.yml

- `kubectl apply -f deployment.yml`

- `kubectl get pods` (se ven 3)

- `kubectl exec -it <podname> -- bash`

- `kubectl exec -it password-api-777c9b99f9-tlpmh -- bash` (en mi caso)

- `curl localhost:3000/password` devuelve algo del tipo `{"password":"!p455w0rd-Pp"}`